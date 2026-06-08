<template>
  <section id="home" class="hero">
    <!-- Left Content -->

    <div class="hero-text">
      <div class="badge">🚀 Available for Internship</div>

      <h1>
        Hi, I'm
        <span class="gradient"> KEO CHANPONLORK </span>
      </h1>
      <h2>
        <span ref="typed"></span>
      </h2>

      <p>
        Fourth-Year Computer Science Student passionate about Mobile
        Development, Backend Development, AI Applications, and building
        impactful software solutions.
      </p>

      <div class="buttons">
        <a href="/KEO CHANPONLOKR-CV.pdf" download class="primary-btn"> Download CV </a>

        <a href="#contact" class="secondary-btn"> Contact Me </a>
      </div>
    </div>

    <!-- Right Side -->

    <div class="profile-wrapper">
      <!-- Floating Technologies -->

      <div
        v-for="tech in techs"
        :key="tech.name"
        class="tech-orb"
        :class="tech.class"
      >
        <img :src="tech.logo" />

        <span class="tooltip">
          {{ tech.name }}
        </span>
      </div>

      <!-- Profile Card -->

      <div class="profile-card">
        <img src="../assets/profile.JPG" alt="Profile" />

        <h3>KEO CHANPONLORK</h3>

        <p class="role">Flutter Developer</p>

        <div class="info">
          <div>📍 Phnom Penh, Cambodia</div>

          <div>🎓 Computer Science Student</div>

          <div>💼 Seeking Internship</div>

          <div>🚀 Open to Flutter Opportunities</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import Typed from "typed.js";
import { onMounted, ref } from "vue";

const typed = ref(null);

onMounted(() => {
  new Typed(typed.value, {
    strings: [
      "Flutter Developer",
      "AI Enthusiast",
      "Computer Science Student",
      "Backend Developer",
    ],

    typeSpeed: 60,
    backSpeed: 40,
    loop: true,
  });
});
const techs = [
  {
    name: "Flutter",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg",
    class: "flutter",
  },

  {
    name: "Vue",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg",
    class: "vue",
  },

  {
    name: "Git",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
    class: "git",
  },

  {
    name: "Spring",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg",
    class: "spring",
  },

  {
    name: "MySQL",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg",
    class: "mysql",
  },

  {
    name: "Docker",
    logo: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg",
    class: "docker",
  },
];
</script>

<style scoped>
.hero {
  min-height: 100vh;

  display: flex;

  justify-content: space-between;

  align-items: center;

  gap: 80px;

  padding: 120px 8%;
}

/* LEFT SIDE */

.hero-text {
  flex: 1;
}

.badge {
  display: inline-block;

  padding: 10px 18px;

  border-radius: 999px;

  background: rgba(255, 255, 255, 0.06);

  backdrop-filter: blur(20px);

  border: 1px solid rgba(255, 255, 255, 0.08);

  margin-bottom: 25px;
}

.hero h1 {
  font-size: 4.5rem;

  margin: 0;
}

.gradient {
  background: linear-gradient(135deg, #00d4ff, #8b5cf6);

  -webkit-background-clip: text;

  -webkit-text-fill-color: transparent;
}

.hero h2 {
  color: #00d4ff;

  margin-top: 15px;
}

.hero p {
  max-width: 600px;

  line-height: 1.8;

  color: #c7c7c7;
}

.buttons {
  margin-top: 30px;

  display: flex;

  gap: 15px;
}

.primary-btn {
  background: linear-gradient(135deg, #00d4ff, #8b5cf6);

  color: white;

  padding: 14px 24px;

  border-radius: 14px;

  text-decoration: none;

  font-weight: 600;

  transition: 0.3s;
}

.primary-btn:hover {
  transform: translateY(-3px);

  box-shadow: 0 0 25px rgba(0, 212, 255, 0.35);
}

.secondary-btn {
  color: white;

  text-decoration: none;

  padding: 14px 24px;

  border-radius: 14px;

  border: 1px solid rgba(255, 255, 255, 0.1);

  background: rgba(255, 255, 255, 0.03);
}

/* RIGHT SIDE */

.profile-wrapper {
  position: relative;

  width: 500px;

  height: 550px;
}

.profile-card {
  position: absolute;

  left: 50%;
  top: 50%;

  transform: translate(-50%, -50%);

  width: 340px;

  padding: 25px;

  text-align: center;

  border-radius: 28px;

  background: rgba(255, 255, 255, 0.05);

  backdrop-filter: blur(20px);

  border: 1px solid rgba(255, 255, 255, 0.08);

  box-shadow: 0 0 40px rgba(0, 212, 255, 0.1);
}
.profile-card {
  border-radius: 32px;

  background: linear-gradient(
    145deg,
    rgba(255, 255, 255, 0.05),
    rgba(255, 255, 255, 0.02)
  );

  position: relative;
}
.profile-card::before {
  content: "";

  position: absolute;

  inset: -1px;

  border-radius: 32px;

  background: linear-gradient(
    135deg,
    rgba(0, 212, 255, 0.3),
    rgba(139, 92, 246, 0.3)
  );

  z-index: -1;
}
.profile-card img {
  width: 220px;
  height: 220px;

  object-fit: cover;

  border-radius: 24px;

  border: 3px solid rgba(255, 255, 255, 0.1);

  box-shadow: 0 0 40px rgba(0, 212, 255, 0.25);
}

.role {
  color: #00d4ff;
}

.info {
  text-align: left;

  margin-top: 20px;

  display: flex;

  flex-direction: column;

  gap: 10px;

  color: #d7d7d7;
}

/* FLOATING BADGES */

.floating {
  position: absolute;

  display: flex;

  align-items: center;

  gap: 10px;

  padding: 10px 18px;

  border-radius: 18px;

  background: rgba(255, 255, 255, 0.06);

  backdrop-filter: blur(20px);

  border: 1px solid rgba(255, 255, 255, 0.08);

  animation: float 4s ease-in-out infinite;
}

.floating img {
  width: 28px;

  height: 28px;
}

.floating span {
  font-size: 0.9rem;

  font-weight: 600;
}

.flutter {
  top: 0;
  left: 50%;

  transform: translateX(-50%);
}

.vue {
  right: 0;
  top: 120px;
}

.git {
  left: 0;
  top: 120px;
}

.spring {
  left: 0;
  bottom: 120px;
}

.mysql {
  right: 0;
  bottom: 120px;
}

.docker {
  left: 50%;
  bottom: 0;

  transform: translateX(-50%);
}

@keyframes float {
  0% {
    transform: translateY(0px);
  }

  50% {
    transform: translateY(-12px);
  }

  100% {
    transform: translateY(0px);
  }
}

@media (max-width: 1000px) {
  .hero {
    flex-direction: column;

    text-align: center;
  }

  .profile-wrapper {
    width: 100%;
  }

  .hero h1 {
    font-size: 3rem;
  }
}
.tech-orb {
  position: absolute;

  width: 70px;
  height: 70px;

  border-radius: 50%;

  display: flex;
  justify-content: center;
  align-items: center;

  background: rgba(255, 255, 255, 0.08);

  backdrop-filter: blur(20px);

  border: 1px solid rgba(255, 255, 255, 0.08);

  box-shadow: 0 0 30px rgba(0, 212, 255, 0.1);

  animation: float 5s ease-in-out infinite;
}

.tech-orb img {
  width: 34px;
  height: 34px;
}

.tooltip {
  position: absolute;

  top: -45px;

  opacity: 0;

  transition: 0.3s;
}

.tech-orb:hover .tooltip {
  opacity: 1;
}
</style>
