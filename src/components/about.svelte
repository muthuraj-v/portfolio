<section id="about">
  <div class="about-grid">
    <h2 class="about-title">About Me</h2>

    <div class="about-content">
      <p>
        I'm a software engineer who enjoys building reliable and scalable
        systems. My work mainly focuses on full-stack development using the MERN
        stack, TypeScript, and C#. I enjoy solving complex problems, designing
        clean system architectures, and understanding how software works at a
        deeper level. Debugging, system design, and writing efficient code are
        parts of development that I genuinely enjoy.
      </p>

      <p>
        I enjoy debugging, system design, I value lifelong learning and
        disciplined growth, and I constantly explore new ways to understand
        complex systems by breaking problems down to their core. Continuous
        learning and improving my debugging skills are central to how I approach
        software engineering.
      </p>
      <p>
        Outside of development, I'm naturally curious about how systems work and
        how technology shapes the world around us. I enjoy exploring new ideas,
        experimenting with tools, and understanding complex problems from
        different perspectives.
      </p>
    </div>
  </div>
</section>

<style>
  section {
    width: 100%;
    min-height: 100vh;
    /* margin: 0 auto; */
    padding-top: 80px;
  }

  .about-grid {
    display: grid;
    grid-template-columns: 200px 1fr;
    gap: 40px;
    align-items: start;
  }

  .about-title {
    font-size: 38px;
    font-weight: 500;
    opacity: 0.9;
  }

  .about-content {
    border-left: 2px solid rgba(255, 255, 255, 0.6);
    padding-left: 40px;
    max-width: 700px;
  }

  .about-content p {
    margin-bottom: 26px;
    line-height: 1.8;
    opacity: 0.75;
    font-size: 16px;
  }
  @media (min-width: 1900px) {
    section {
      width: 90%;
      min-height: 80vh;
      margin: 0 auto;
      padding-top: 180px;
    }
  }
  @media (max-width: 768px) {
    .about-grid {
      grid-template-columns: 1fr;
      gap: 20px;
    }

    .about-content {
      border-left: none;
      border-top: 2px solid rgba(255, 255, 255, 0.6);
      padding-left: 0;
      padding-top: 20px;
    }
  }
</style>
