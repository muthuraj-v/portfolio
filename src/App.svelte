<script lang="ts">
  import "@fontsource/inter";
  import { onMount } from "svelte";
  import gsap from "gsap";
  import Main from "./main.svelte";

  let video;
  let overlay;

  onMount(() => {
    gsap.to(overlay, {
      opacity: 0.75,
      duration: 6,
      repeat: -1,
      yoyo: true,
      ease: "sine.inOut",
    });
  });
</script>

<main>
  <video
    autoplay
    muted
    loop
    id="bg-video"
    preload="auto"
    poster="image/poster.webp"
    bind:this={video}
  >
    <source
      src="video/248954cba9bc08b6e16c676f5c1814ff823af907.mp4"
      type="video/mp4"
    />
  </video>

  <div class="overlay" bind:this={overlay}></div>

  <Main />
</main>
