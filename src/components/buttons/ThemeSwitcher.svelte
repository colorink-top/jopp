<script lang="ts">
  import { browser } from "$app/environment";
  import IconButton from "./IconButton.svelte";

  export let size: "small" | "medium" | "large" = "small";

  let isDarkMode: boolean = false;

  function setDarkTheme() {
    const root: HTMLElement = document.documentElement;
    root.classList.add("dark");
  }

  function setLightTheme() {
    const root: HTMLElement = document.documentElement;
    root.classList.remove("dark");
  }

  function toggleDarkTheme() {
    if (isDarkMode === false) {
      isDarkMode = true;
      setDarkTheme();
    }
  }

  function toggleLightTheme() {
    if (isDarkMode === true) {
      isDarkMode = false;
      setLightTheme();
    }
  }

  function togglePreferredTheme() {
    if (browser) {
      const root: HTMLElement = document.documentElement;
      if (window.matchMedia("(prefers-color-scheme: dark)").matches) {
        root.classList.add("dark");
        isDarkMode = true;
      } else {
        root.classList.remove("dark");
        isDarkMode = false;
      }
    }
  }
</script>

<div class="flex justify-center items-center gap-2">
  <IconButton
    icon="light_mode"
    {size}
    variant="secondary"
    on:click={toggleLightTheme}
    tooltip="Toggle Light Mode"
  />
  <IconButton
    icon="dark_mode"
    {size}
    variant="secondary"
    on:click={toggleDarkTheme}
    tooltip="Toggle Dark Mode"
  />
  <IconButton
    icon="computer"
    {size}
    variant="secondary"
    on:click={togglePreferredTheme}
    tooltip="Toggle System Default"
  />
</div>
