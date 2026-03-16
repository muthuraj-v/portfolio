<script>
  import { onMount } from "svelte";
  import gsap from "gsap";

  let hero;
  // @ts-ignore
  let items = [];

  onMount(() => {
    // @ts-ignore
    gsap.from(items, {
      y: 80,
      opacity: 0,
      duration: 1,
      stagger: 0.2,
      ease: "power3.out",
    });
  });
</script>

<div>
  <section class="hero" bind:this={hero}>
    <div class="hero-left">
      <h1 bind:this={items[0]}>Raghav</h1>
      <h3 bind:this={items[1]}>Software Engineer</h3>

      <p bind:this={items[2]}>
        Building scalable solutions, solving complex problems, and evolving with
        emerging technologies.
      </p>

      <div class="skills" bind:this={items[3]}>
        <span>MERN</span>
        <span>TypeScript</span>
        <span>C#</span>
        <span>Go</span>
        <span>IoT</span>
      </div>
    </div>
  </section>
  <div class="scroll-indicator" bind:this={items[5]}>
    <a href="#about" aria-label="about">
      <svg
        fill="#fff"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 30.727 30.727"
      >
        <path
          d="M29.994,10.183L15.363,24.812L0.733,10.184c-0.977-0.978-0.977-2.561,0-3.536c0.977-0.977,2.559-0.976,3.536,0 l11.095,11.093L26.461,6.647c0.977-0.976,2.559-0.976,3.535,0C30.971,7.624,30.971,9.206,29.994,10.183z"
        ></path>
      </svg>
    </a>
  </div>
</div>

<style>
  .hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 100px;
    padding: 0 20px;
  }

  .hero-left h1 {
    font-size: clamp(42px, 6vw, 60px);
    margin-bottom: 10px;
  }

  .hero-left h3 {
    font-weight: 300;
    margin-bottom: 20px;
    opacity: 0.8;
    font-size: clamp(18px, 3vw, 22px);
  }

  .hero-left p {
    max-width: 420px;
    line-height: 1.6;
    opacity: 0.7;
    margin-bottom: 20px;
    font-size: clamp(14px, 2.4vw, 16px);
  }

  .skills {
    display: flex;
    justify-content: flex-start;
    gap: 12px;
    flex-wrap: wrap;
    max-width: 450px;
  }

  .skills span {
    border: 1px solid rgba(255, 255, 255, 0.2);
    padding: 8px 16px;
    border-radius: 10px;
    font-size: 14px;
    backdrop-filter: blur(4px);
    transition: 0.3s ease;
  }

  /* .skills span:hover {
    border-color: white;
    transform: translateY(-3px);
  } */

  .scroll-indicator {
    display: flex;
    justify-content: center;
    width: 100%;
    margin: 80px 0 20px 0;
  }

  .scroll-indicator svg {
    height: 32px;
    width: auto;
    animation: bounce 1.6s infinite;
    opacity: 0.9;
  }

  @media (min-width: 640px) {
    .scroll-indicator svg {
      height: 40px;
    }

    .scroll-indicator {
      margin-top: 24px;
    }
  }
  @media (min-width: 1900px) {
    .hero {
      height: 70dvh;
    }
  }
  @media (max-width: 768px) {
    .hero {
      flex-direction: column;
      align-items: flex-start;
      margin-bottom: 60px;
    }

    .hero-left p {
      max-width: 100%;
    }

    .skills {
      max-width: 100%;
    }
  }

  @keyframes bounce {
    0%,
    100% {
      transform: translateY(0);
    }

    50% {
      transform: translateY(10px);
    }
  }
</style>
