<script lang="ts">
  import { onMount } from "svelte";
  import gsap from "gsap";

  let group: gsap.TweenTarget;
  let fullText: gsap.TweenTarget;

  function hoverIn() {
    gsap.to(fullText, {
      opacity: 1,
      x: 0,
      duration: 0.5,
      ease: "power2.out",
    });
  }

  function hoverOut() {
    gsap.to(fullText, {
      opacity: 0,
      x: -20,
      duration: 0.4,
      ease: "power2.in",
    });
  }

  onMount(() => {
    gsap.set(fullText, { opacity: 0, x: -20 });
  });
</script>

<div class="center">
  <!-- svelte-ignore a11y_no_static_element_interactions -->
  <svg
    xmlns="http://www.w3.org/2000/svg"
    width="170"
    height="40"
    viewBox="0 0 400 100"
    class="logo-svg"
    on:mouseenter={hoverIn}
    on:mouseleave={hoverOut}
  >
    <g bind:this={group}>
      <text x="50" y="60" class="first-letter">M</text>
      <text x="110" y="60" bind:this={fullText} class="full-text">ISTY</text>
    </g>
  </svg>
</div>

<style>
  .center {
    max-width: 170px;
  }

  .logo-svg {
    cursor: pointer;
  }

  text {
    font-size: 60px;
    font-family: "Inter";
    fill: whitesmoke;
    font-weight: 700;
  }

  .first-letter {
    letter-spacing: 2px;
  }

  .full-text {
    letter-spacing: 3px;
  }
</style>
