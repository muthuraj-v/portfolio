<script lang="ts">
  import { onMount } from "svelte";
  import gsap from "gsap";

  let footerEl;

  onMount(() => {
    gsap.from(footerEl, {
      opacity: 0,
      y: 30,
      duration: 0.8,
      ease: "power3.out",
    });
  });
</script>

<footer bind:this={footerEl}>
  <div class="top">
    <!-- Left: Email -->
    <div class="email">
      <span class="icon">✉</span>
      <a href="mailto:muthurajkpr3@gmail.com"> muthurajkpr3@gmail.com </a>
    </div>

    <div class="socials">
      <!-- Instagram -->

      <!-- GitHub -->
      <a
        href="https://github.com/muthuraj-v"
        target="_blank"
        aria-label="GitHub"
      >
        <svg viewBox="0 0 24 24" fill="currentColor">
          <path
            d="M12 .5C5.73.5.5 5.73.5 12c0 5.08 3.29 9.39 7.86 10.91.58.1.79-.25.79-.56v-2.17c-3.2.7-3.88-1.54-3.88-1.54-.52-1.33-1.28-1.69-1.28-1.69-1.04-.71.08-.7.08-.7 1.15.08 1.75 1.18 1.75 1.18 1.02 1.74 2.67 1.24 3.32.95.1-.74.4-1.24.73-1.52-2.55-.29-5.23-1.27-5.23-5.65 0-1.25.45-2.27 1.18-3.07-.12-.29-.51-1.47.11-3.06 0 0 .96-.31 3.15 1.17a10.9 10.9 0 012.87-.39c.97 0 1.95.13 2.87.39 2.19-1.48 3.15-1.17 3.15-1.17.62 1.59.23 2.77.11 3.06.73.8 1.18 1.82 1.18 3.07 0 4.39-2.68 5.35-5.24 5.64.41.35.77 1.03.77 2.08v3.08c0 .31.21.67.8.56A11.51 11.51 0 0023.5 12C23.5 5.73 18.27.5 12 .5z"
          />
        </svg>
      </a>

      <span>/</span>

      <!-- LinkedIn -->
      <a
        href="https://www.linkedin.com/in/muthuraj-v"
        target="_blank"
        aria-label="LinkedIn"
      >
        <svg viewBox="0 0 24 24" fill="currentColor">
          <path
            d="M4.98 3.5C4.98 4.88 3.87 6 2.49 6S0 4.88 0 3.5 1.11 1 2.49 1s2.49 1.12 2.49 2.5zM.5 8h4v12h-4V8zm7.5 0h3.8v1.64h.05c.53-1 1.84-2.05 3.79-2.05 4.05 0 4.8 2.66 4.8 6.12V20h-4v-5.73c0-1.37-.02-3.14-1.92-3.14-1.92 0-2.21 1.5-2.21 3.04V20h-4V8z"
          />
        </svg>
      </a>
      <span>/</span>

      <a
        href="https://www.linkedin.com/in/muthuraj-v"
        target="_blank"
        aria-label="Instagram"
      >
        <svg viewBox="0 0 24 24" fill="none">
          <rect
            x="3"
            y="3"
            width="18"
            height="18"
            rx="5"
            stroke="currentColor"
            stroke-width="1.5"
          />
          <circle
            cx="12"
            cy="12"
            r="4"
            stroke="currentColor"
            stroke-width="1.5"
          />
          <circle cx="17" cy="7" r="1" fill="currentColor" />
        </svg>
      </a>
    </div>
  </div>

  <div class="divider"></div>

  <!-- Bottom: Credit -->
  <div class="bottom">
    Made by <span>MISTY 💖</span>
  </div>
</footer>

<style>
  footer {
    margin-top: 80px;
    padding: 30px 20px;
    border-radius: 16px;

    /* Gradient background like your image */
    background: linear-gradient(
      90deg,
      rgba(0, 0, 0, 0.9),
      rgba(40, 40, 40, 0.6),
      rgba(0, 0, 0, 0.9)
    );

    border: 1px solid rgba(255, 255, 255, 0.08);
    backdrop-filter: blur(12px);
  }

  .top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 10px;
  }

  .email {
    display: flex;
    align-items: center;
    gap: 10px;
    opacity: 0.8;
  }

  .email a {
    text-decoration: none;
    color: inherit;
  }

  .icon {
    background: rgba(255, 255, 255, 0.08);
    padding: 8px;
    border-radius: 50%;
  }
  .socials {
    display: flex;
    align-items: center;
    gap: 10px;
    opacity: 0.8;
  }
  .socials a {
    display: flex;
    align-items: center;
    justify-content: center;

    width: 32px;
    height: 32px;

    border-radius: 50%;
    background: rgba(255, 255, 255, 0.05);

    transition: all 0.3s ease;
  }

  .socials svg {
    width: 16px;
    height: 16px;
    opacity: 0.8;
  }

  .socials a:hover {
    transform: translateY(-3px);
    background: rgba(255, 255, 255, 0.1);
  }

  .socials a:hover svg {
    opacity: 1;
  }
  .divider {
    margin: 20px 0;
    height: 1px;
    background: rgba(255, 255, 255, 0.1);
  }

  .bottom {
    text-align: center;
    opacity: 0.7;
    font-size: 14px;
  }

  .bottom span {
    font-weight: 600;
    color: white;
  }

  @media (max-width: 768px) {
    .top {
      flex-direction: column;
      align-items: flex-start;
    }

    .socials {
      align-self: flex-end;
    }
  }
</style>
