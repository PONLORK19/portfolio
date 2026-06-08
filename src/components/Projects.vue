<template>
  <section id="projects">
    <h2 class="section-title">Projects</h2>

    <div class="projects-grid">
      <div class="project-card">
        <h3>Phone Shop App</h3>
        <p>Flutter + Firebase</p>
      </div>

      <div class="project-card">
        <h3>Java Platformer Game</h3>
        <p>Java Swing</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section-title {
  font-size: 3rem;
  text-align: center;

  background: linear-gradient(135deg, #00d4ff, #8b5cf6);

  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.project-card {
  background: rgba(255, 255, 255, 0.05);

  backdrop-filter: blur(18px);

  border: 1px solid rgba(255, 255, 255, 0.08);

  border-radius: 24px;

  overflow: hidden;

  transition: 0.3s;
}

.project-card:hover {
  transform: translateY(-10px);

  box-shadow: 0 0 30px rgba(139, 92, 246, 0.2);
}
</style>
