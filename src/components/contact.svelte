<script lang="ts">
  import { onMount } from "svelte";
  import gsap from "gsap";

  let contactEl;

  onMount(() => {
    gsap.from(contactEl, {
      opacity: 0,
      y: 30,
      duration: 0.8,
      ease: "power3.out",
    });
  });
</script>

<section id="contact" bind:this={contactEl}>
  <h2 class="contact-title">Love to hear from you, Get in touch 👋</h2>

  <form class="contact-form">
    <div class="form-row">
      <div class="form-group">
        <label for="name">Your Name</label>
        <input type="text" id="name" />
      </div>
      <div class="form-group">
        <label for="email">Email Address</label>
        <input type="email" id="email" />
      </div>
    </div>
    <div class="form-group">
      <label for="message">Message</label>
      <textarea id="message" rows="5" placeholder="Your message..."></textarea>
    </div>
    <button type="submit" on:click={(event) => event.preventDefault()}
      >Send Message</button
    >
  </form>
</section>

<style>
  section#contact {
    margin: 50px;
    padding: 80px 20px;
    border-radius: 16px;
    background: linear-gradient(
      90deg,
      rgba(0, 0, 0, 0.9),
      rgba(40, 40, 40, 0.6),
      rgba(0, 0, 0, 0.9)
    );
    border: 1px solid rgba(255, 255, 255, 0.08);
    backdrop-filter: blur(12px);
    max-width: 900px;
    margin-top: 70px;
  }

  .contact-title {
    font-size: 36px;
    font-weight: 600;
    text-align: center;
    margin-bottom: 40px;
    opacity: 0.9;
  }

  .contact-form {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .form-row {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    flex: 1;
  }

  .form-group label {
    margin-bottom: 6px;
    opacity: 0.8;
    font-size: 14px;
  }

  .form-group input,
  .form-group textarea {
    padding: 14px 16px;
    border-radius: 12px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(10px);
    color: inherit;
    font-size: 16px;
    transition: 0.3s;
  }

  .form-group input:focus,
  .form-group textarea:focus {
    outline: none;
    border-color: rgba(255, 255, 255, 0.3);
    background: rgba(255, 255, 255, 0.08);
  }

  button {
    align-self: flex-start;
    padding: 12px 28px;
    border-radius: 12px;
    background: rgba(255, 255, 255, 0.08);
    border: 1px solid rgba(255, 255, 255, 0.1);
    color: inherit;
    font-weight: 600;
    cursor: pointer;
    transition: 0.3s;
  }

  button:hover {
    background: rgba(255, 255, 255, 0.12);
    transform: translateY(-3px);
  }

  @media (max-width: 768px) {
    .form-row {
      flex-direction: column;
    }
  }
</style>
