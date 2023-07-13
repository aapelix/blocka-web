<script>
  let scale = 1;
  export let title;
  export let onClick;
</script>

{#if onClick}
  <button
    class="bg-blue-500 w-40 h-11 text-xl rounded-lg m-3 duration-300"
    style="transform: scale({scale});"
    on:click={() => window.location.assign("#download")}
    on:mousedown={() => (scale = 0.9)}
    on:mouseup={() => (scale = 1)}
    on:mouseenter={() => (scale = 1.1)}
    on:mouseleave={() => (scale = 1)}>{title}</button
  >
{:else}
  <button
    class="bg-blue-500 w-40 h-11 text-xl rounded-lg m-3 duration-300"
    style="transform: scale({scale});"
    on:mousedown={() => (scale = 0.9)}
    on:mouseup={() => (scale = 1)}
    on:mouseenter={() => (scale = 1.1)}
    on:mouseleave={() => (scale = 1)}>{title}</button
  >
{/if}
