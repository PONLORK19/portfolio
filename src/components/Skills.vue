<template>
  <section id="skills">
    <h2 class="title">Tech Stack</h2>

    <div class="skills-grid">
      <div class="skill-card" v-for="skill in skills" :key="skill.name">
        <img :src="skill.logo" :alt="skill.name" />

        <span>
          {{ skill.name }}
        </span>
      </div>
    </div>
  </section>
</template>

<script setup>
const skills = [
  {
    name: "Flutter",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg",
  },

  {
    name: "Dart",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dart/dart-original.svg",
  },

  {
    name: "Firebase",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg",
  },
  {
    name: "Vue.js",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg",
  },
  {
    name: "C++",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg",
  },

  {
    name: "C",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg",
  },
  {
    name: "Java",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg",
  },
  {
    name: "JavaScript",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
  },

  {
    name: "Next.js",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg",
  },

  {
    name: "Spring",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg",
  },

  {
    name: "MySQL",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg",
  },

  {
    name: "Docker",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg",
  },

  {
    name: "Git",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
  },
];
</script>

<style scoped>
.title {
  text-align: center;
  margin-bottom: 50px;
}

.skills-grid {
  display: grid;

  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));

  gap: 20px;
}

.skill-card {
  background: rgba(255, 255, 255, 0.05);

  backdrop-filter: blur(18px);

  border: 1px solid rgba(255, 255, 255, 0.08);

  border-radius: 24px;

  padding: 30px;

  display: flex;

  flex-direction: column;

  align-items: center;

  gap: 15px;

  transition: 0.3s;
}

.skill-card:hover {
  transform: translateY(-8px);

  box-shadow: 0 0 25px rgba(0, 212, 255, 0.15);
}

.skill-card img {
  width: 60px;
  height: 60px;
}

.skill-card span {
  font-size: 1rem;
}
</style>
