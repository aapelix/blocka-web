<script>
  export let title;
  export let url;
  export let imgUrl;
  export let description;
  export let date;
</script>

<div class="flex justify-center">
  <button
    on:click={() => (window.location.href = url)}
    class="text-left bg-[#3a3a3a] rounded-md w-60 h-56 mb-5 mt-5 m-2 hover:scale-110 duration-300"
  >
    <div class="p-2">
      <p class="text-gray-300">{date}</p>
      <h1 class="text-xl font-bold m-1">{title}</h1>
      <div>
        <img
          src={imgUrl}
          alt="Patch Note"
          class="w-[calc(100%-1px)] h-32 rounded-lg"
        />
        <p>{description}</p>
      </div>
    </div>
  </button>
</div>
