<script>
  let isOpen = false;
  export let title;

  import { slide } from "svelte/transition";
</script>

<div class="flex justify-center m-3">
  <div class="bg-[#222] w-96 p-5 rounded-lg">
    <button
      class="text-2xl hover:text-gray-300 duration-300"
      on:click={() => (isOpen = !isOpen)}>{title}</button
    >

    {#if isOpen}
      <div transition:slide>
        <slot name="details" />
      </div>
    {/if}
  </div>
</div>
