<script lang="ts">
  import ProjectCard from "../lib/project_card.svelte";
</script>

<section class="projects">
  <h4>PROJECTS</h4>

  <div class="project-grid">
    <ProjectCard
      title="Pomodoro+"
      description="Pomodoro timer"
      stack="Svelte · Wails · Go"
      link="https://github.com/muthuraj-v/Pomodoro"
    />

    <ProjectCard
      title="Manga Reader"
      description="MangaDex API Comic Reader"
      stack="React · Mangadex API"
      link="https://github.com/muthuraj-v/MangaReader"
    />

    <ProjectCard
      title="Expense Tracker"
      description="Money Management"
      stack="React · TypeScript · Nodejs"
      link="http://github.com/muthuraj-v/expense-tracker"
    />
  </div>
</section>

<style>
  .projects {
    margin-top: 80px;
  }

  .projects h4 {
    margin-bottom: 30px;
    opacity: 0.7;
    letter-spacing: 2px;
  }

  .project-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 25px;
  }

  @media (max-width: 900px) {
    .project-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 600px) {
    .project-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
