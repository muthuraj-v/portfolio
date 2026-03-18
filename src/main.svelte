<script lang="ts">
  import About from "./components/about.svelte";
  import Content from "./components/content.svelte";
  import Headers from "./components/headers.svelte";
  import Projects from "./components/projects.svelte";
  import Skills from "./components/skills.svelte";
</script>

<main class="container">
  <Headers />
  <Content />
  <About />
  <Skills />
  <Projects />
</main>

<style>
  .container {
    width: min(1100px, 90%);
    margin: 0 auto;
    padding: 20px 40px;
  }
  .container::-webkit-scrollbar-button {
    display: none;
  }
  @media (max-width: 768px) {
    .container {
      padding: 20px;
      width: 92%;
    }
  }

  @media (max-width: 480px) {
    .container {
      padding: 16px;
      width: 94%;
    }
  }
</style>
