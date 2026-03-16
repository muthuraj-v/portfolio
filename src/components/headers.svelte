<script>
  import { onMount } from "svelte";
  import gsap from "gsap";
  import Logo from "../lib/logo.svelte";

  let items = [];

  onMount(() => {
    gsap.from(items, {
      y: 20,
      opacity: 0,
      stagger: 0.1,
      duration: 0.6,
      ease: "power3.out",
    });

    items.forEach((item) => {
      item.addEventListener("mouseenter", () => {
        gsap.to(item, {
          y: -5,
          opacity: 1,
          duration: 0.3,
          ease: "power2.out",
        });
      });

      item.addEventListener("mouseleave", () => {
        gsap.to(item, {
          y: 0,
          opacity: 0.8,
          duration: 0.3,
          ease: "power2.out",
        });
      });
    });
  });
</script>

<nav>
  <Logo />

  <ul>
    <a href="#about"> <li bind:this={items[0]}>About</li></a>
    <a href="#projects"> <li bind:this={items[1]}>Projects</li></a>
    <a href="#contact">
      <li bind:this={items[2]}>Contact</li>
    </a>
  </ul>
</nav>

<style>
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 40px;
    padding: 0 20px;
  }

  ul {
    display: flex;
    gap: 40px;
    list-style: none;
  }

  li {
    opacity: 0.8;
    cursor: pointer;
    transition: color 0.2s ease;
  }

  li:hover {
    color: white;
  }

  @media (max-width: 768px) {
    ul {
      gap: 20px;
      font-size: 14px;
    }
  }
</style>
