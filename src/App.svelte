<script lang="ts">
  import "@fontsource/inter";
  import Main from "./main.svelte";
</script>

<main>
  <video
    autoplay
    muted
    loop
    id="bg-video"
    preload="auto"
    poster="image/poster.webp"
  >
    <source src="video/bg.mp4" type="video/mp4" />
  </video>

  <div class="overlay"></div>

  <Main />
</main>

<style>
  main::-webkit-scrollbar-button {
    display: none;
  }
</style>
