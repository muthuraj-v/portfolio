<section id="skills">
  <div class="skills-grid">
    <h2 class="skills-title">Professional Skillset</h2>

    <div class="skills-content">
      <div class="icons-grid">
        <div class="icon-card">
          <img src="icons/javascript1.svg" alt="JavaScript" />
          <span>JavaScript</span>
        </div>
        <div class="icon-card">
          <img src="icons/typescript.svg" alt="TypeScript" title="TypeScript" />
          <span>TypeScript</span>
        </div>
        <div class="icon-card">
          <img src="icons/csharp.svg" alt="C#" title="C#" />
          <span>C#</span>
        </div>
        <div class="icon-card">
          <img src="icons/node.svg" alt="Node.js" title="Node.js" />
          <span>Node.js</span>
        </div>
        <div class="icon-card">
          <img src="icons/react.svg" alt="React" title="React" />
          <span>React</span>
        </div>
        <div class="icon-card">
          <img src="icons/svelte.svg" alt="Svelte" title="Svelte" />
          <span>Svelte</span>
        </div>
        <div class="icon-card">
          <img src="icons/css.svg" alt="CSS" title="CSS" />
          <span>CSS</span>
        </div>
        <div class="icon-card">
          <img src="icons/mongodb.svg" alt="MongoDB" title="MongoDB" />
          <span>MongoDB</span>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  section {
    color: #fff;
  }
  .skills-grid {
    display: grid;
    grid-template-columns: 200px 1fr;
    gap: 40px;
    align-items: start;
    justify-content: center;
  }

  .skills-title {
    font-size: 38px;
    font-weight: 500;
    opacity: 0.9;
  }

  .skills-content {
    border-left: 2px solid rgba(255, 255, 255, 0.6);
    padding-left: 40px;
    max-width: 700px;
  }

  .icons-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    gap: 30px;
  }

  .icon-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    opacity: 0.85;
    transition:
      transform 0.2s ease,
      opacity 0.2s ease;
  }

  .icon-card img {
    width: 42px;
    height: 42px;
    margin-bottom: 10px;

    filter: invert(1);
    /* drop-shadow(0 0 6px rgba(255, 255, 255, 0.5)) */
  }

  .icon-card span {
    font-size: 14px;
    opacity: 0.7;
    color: #fff;
  }
</style>
