<script lang="ts">
  import Text from "../typography/Text.svelte";
  import Logo from "../icons/Logo.svelte";
  import LinkButton from "../buttons/LinkButton.svelte";
</script>

<header
  class="
    p-4
    flex
    justify-center
    items-center
    z-10"
>
  <div class="w-full max-w-5xl flex justify-between items-center">
    <div class="flex justify-center items-center gap-2">
      <div class="w-6 aspect-square text-sky-500 dark:text-slate-200">
        <Logo />
      </div>
      <div class="hidden sm:inline text-slate-800 dark:text-slate-200">
        <Text as="h6">snw</Text>
      </div>
    </div>
    <div class="flex justify-center items-center gap-4">
      <nav class="flex justify-center items-center gap-4">
      </nav>
    </div>
  </div>
</header>
