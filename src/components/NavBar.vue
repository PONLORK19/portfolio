<template>
  <header class="navbar-wrapper">
    <nav class="navbar">
      <div class="left">
        <h2 class="logo">Ponlork.dev</h2>

        <div class="status">
          <span class="dot"></span>
          Available for Internship
        </div>
      </div>

      <div class="nav-links">
        <a
          v-for="item in links"
          :key="item.id"
          :href="`#${item.id}`"
          :class="{ active: activeSection === item.id }"
        >
          {{ item.label }}
        </a>
      </div>

      <a href="/portfolio/KEO CHANPONLORK-CV.pdf" download class="resume-btn"> Resume </a>
    </nav>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const activeSection = ref("home");

const links = [
  { id: "home", label: "Home" },
  { id: "about", label: "About" },
  { id: "skills", label: "Skills" },
  { id: "projects", label: "Projects" },
  { id: "contact", label: "Contact" },
];

let observer;

onMounted(() => {
  const sections = document.querySelectorAll("section[id]");

  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          activeSection.value = entry.target.id;
        }
      });
    },
    {
      threshold: 0.4,
    },
  );

  sections.forEach((section) => {
    observer.observe(section);
  });
});

onUnmounted(() => {
  observer.disconnect();
});
</script>

<style scoped>
.navbar-wrapper {
  position: fixed;
  top: 20px;
  left: 0;
  width: 100%;
  display: flex;
  justify-content: center;
  z-index: 9999;
}

.navbar {
  width: 92%;
  max-width: 1300px;

  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 14px 22px;

  border-radius: 24px;

  background: rgba(255, 255, 255, 0.06);

  backdrop-filter: blur(24px);
  -webkit-backdrop-filter: blur(24px);

  border: 1px solid rgba(255, 255, 255, 0.08);

  box-shadow:
    0 8px 32px rgba(0, 0, 0, 0.35),
    inset 0 1px 0 rgba(255, 255, 255, 0.08);
}

.left {
  display: flex;
  align-items: center;
  gap: 16px;
}

.logo {
  background: linear-gradient(135deg, #00d4ff, #8b5cf6);

  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;

  font-size: 1.5rem;
}
.active {
  background: linear-gradient(
    135deg,
    rgba(0, 212, 255, 0.15),
    rgba(139, 92, 246, 0.15)
  );

  color: white;
}

.status {
  display: flex;
  align-items: center;
  gap: 8px;

  color: #b8b8b8;
  font-size: 0.85rem;
}

.dot {
  width: 8px;
  height: 8px;

  border-radius: 50%;

  background: #00ff88;

  box-shadow:
    0 0 10px #00ff88,
    0 0 20px #00ff88;
}

.nav-links {
  display: flex;
  gap: 14px;
}

.nav-links a {
  text-decoration: none;

  color: rgba(255, 255, 255, 0.7);

  padding: 10px 16px;

  border-radius: 12px;

  transition: 0.3s;
}

.nav-links a:hover {
  color: white;

  background: rgba(255, 255, 255, 0.05);
}

.nav-links a.active {
  color: white;

  background: linear-gradient(
    135deg,
    rgba(0, 212, 255, 0.15),
    rgba(139, 92, 246, 0.15)
  );

  border: 1px solid rgba(255, 255, 255, 0.08);

  backdrop-filter: blur(12px);
}
.resume-btn {
  padding: 10px 18px;

  border-radius: 12px;

  text-decoration: none;

  color: white;

  background: linear-gradient(135deg, #00d4ff, #8b5cf6);
  transition: 0.3s;
}

.resume-btn:hover {
  transform: translateY(-2px);

  box-shadow: 0 0 25px rgba(0, 212, 255, 0.35);
}

@media (max-width: 900px) {
  .status {
    display: none;
  }

  .nav-links {
    display: none;
  }
}
</style>
