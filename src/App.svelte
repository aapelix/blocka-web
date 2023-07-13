<script>
  import { fly } from "svelte/transition";
  import Accordion from "./lib/Accordion.svelte";
  import Button from "./lib/Button.svelte";
  import Navbar from "./lib/Navbar.svelte";
  import Note from "./lib/Note.svelte";

  let scroll;

  let debug = false;
</script>

<svelte:window bind:scrollY={scroll} />

<Navbar />
{#if debug}
  <p class="fixed top-10">{scroll}</p>
{/if}
<section class="m-24">
  <div class="m-10">
    <h1 class="text-6xl m-2 font-bold">Blocka</h1>
    <p class="mb-4">Free, open-source and small Minecraft Launcher</p>
    <Button title="Download!" onClick={true} />
  </div>
</section>
<section id="patchnotes" class="flex justify-center flex-wrap m-5">
  <Note
    title="1.0.0"
    url="/1.0.0"
    imgUrl="/patch-notes/SMP3.png"
    description="The release of Blocka!"
    date="12.7.2023"
  />
  <Note
    title="???"
    url="/???"
    imgUrl="/patch-notes/blurry.png"
    description="Coming soon!"
    date="12.7.2023"
  />
  <Note
    title="???"
    url="/???"
    imgUrl="/patch-notes/blurry.png"
    description="Coming soon!"
    date="12.7.2023"
  />
  <Note
    title="???"
    url="/???"
    imgUrl="/patch-notes/blurry.png"
    description="Coming soon!"
    date="12.7.2023"
  />
  <Note
    title="???"
    url="/???"
    imgUrl="/patch-notes/blurry.png"
    description="Coming soon!"
    date="12.7.2023"
  />
</section>
<section class="flex justify-center flex-col items-center">
  <h1 class="text-2xl font-bold">Made with:</h1>
  <div class="flex flex-wrap w-max text-center">
    <img src="/rust.png" alt="" class="w-24 object-contain" />
    <img src="/tauri.png" alt="" class="w-24 object-contain" />
    <img src="/svelte.png" alt="" class="w-24 object-contain" />
  </div>
</section>
<section id="gallery">
  {#if scroll >= 29}
    <div transition:fly={{ x: 100 }}>
      <h1 class="text-2xl font-bold m-3">Gallery</h1>
      <div class="flex justify-center">
        <div class="bg-[#292929] rounded-lg">
          <div class="grid-list">
            <img
              class="h-44 m-2 rounded-lg"
              src="/patch-notes/SMP3.png"
              alt=""
            />
            <img
              class="h-44 m-2 rounded-lg"
              src="/patch-notes/SMP3.png"
              alt=""
            />
            <img
              class="h-44 m-2 rounded-lg"
              src="/patch-notes/SMP3.png"
              alt=""
            />
            <img
              class="h-44 m-2 rounded-lg"
              src="/patch-notes/SMP3.png"
              alt=""
            />
            <img
              class="h-44 m-2 rounded-lg"
              src="/patch-notes/SMP3.png"
              alt=""
            />
            <img
              class="h-44 m-2 rounded-lg"
              src="/patch-notes/SMP3.png"
              alt=""
            />
            <img
              class="h-44 m-2 rounded-lg"
              src="/patch-notes/SMP3.png"
              alt=""
            />
            <img
              class="h-44 m-2 rounded-lg"
              src="/patch-notes/SMP3.png"
              alt=""
            />
          </div>
        </div>
      </div>
    </div>
  {/if}
</section>

<section id="download" class="m-5">
  <h1 class="text-3xl font-bold">Downloads</h1>
  <Accordion title="Download (Windows)">
    <div slot="details">
      <Button onClick={false} title="Download (.msi)" />
      <Button onClick={false} title="Download (.exe)" />
    </div>
  </Accordion>
  <Accordion title="Download (Linux)">
    <div slot="details">
      <Button onClick={false} title="Download (.iso)" />
    </div>
  </Accordion>
</section>

<section class="bg-[#222] pt-10 pb-5">
  <div>
    <h1 class="text-3xl font-semibold">Blocka</h1>
    <div class="flex flex-wrap justify-center text-xl items-center text-left">
      <ul class="m-2">
        <li class="text-gray-400 hover:text-white duration-300">
          <a href="#patchnotes">Patch Notes</a>
        </li>
        <li class="text-gray-400 hover:text-white duration-300">
          <a href="#gallery">Gallery</a>
        </li>
        <li class="text-gray-400 hover:text-white duration-300">
          <a href="#download">Download</a>
        </li>
      </ul>
      <ul class="m-2">
        <li class="text-gray-400 hover:text-white duration-300">
          <a href="#about">About</a>
        </li>
        <li class="text-gray-400 hover:text-white duration-300">
          <a href="#faq">FAQ</a>
        </li>
        <li class="text-gray-400 hover:text-white duration-300">
          <a href="#contact">Contact</a>
        </li>
      </ul>
      <ul class="m-2">
        <li class="text-gray-400 hover:text-white duration-300">
          <a href="/discord">Discord</a>
        </li>
        <li class="text-gray-400 hover:text-white duration-300">
          <a href="/github">Github</a>
        </li>
        <li class="text-gray-400 hover:text-white duration-300">
          <a href="/twitter">Twitter</a>
        </li>
      </ul>
    </div>
  </div>
</section>
