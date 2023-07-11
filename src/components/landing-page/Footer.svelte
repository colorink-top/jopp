<script lang="ts">
  import Text from "../typography/Text.svelte";
</script>

<footer
  class="w-full bg-slate-500 dark:bg-slate-900 flex flex-col justify-center items-center"
>
  <div
    class="w-full flex justify-center items-center bg-slate-300 dark:bg-slate-700"
  >
    <div
      class="w-full max-w-5xl p-4 flex flex-col gap-2 sm:flex-row sm:justify-between"
    >
      <Text as="legend"
        >&copy; Copyright 2023, Story Writer. All Rights Reserved</Text
      >
      <Text as="legend">Made with passion</Text>
    </div>
  </div>
</footer>
