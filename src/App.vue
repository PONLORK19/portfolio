<template>
  <div class="app" id="home" data-aos="fade-up"> 
    <Navbar />
    <Hero />
    <About />
    <Skills />
    <Projects />
    <Experience />
    <Contact />
  </div>
</template>

<script setup>
import Navbar from "./components/NavBar.vue";
import Hero from "./components/Hero.vue";
import About from "./components/About.vue";
import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";
import Experience from "./components/Experience.vue";
import Contact from "./components/Contact.vue";
</script>

<style>
html {
  scroll-behavior: smooth;
}

bbody {
  background: #030712;
  overflow-x: hidden;
}

body {
  margin: 0;
  color: white;
  background: #050816;
  font-family: Inter, sans-serif;
  overflow-x: hidden;
}

body::before {
  content: "";

  position: fixed;

  width: 700px;
  height: 700px;

  top: -250px;
  left: -250px;

  background: #00d4ff;

  filter: blur(180px);

  opacity: 0.18;

  z-index: -1;
}

body::after {
  content: "";

  position: fixed;

  width: 700px;
  height: 700px;

  bottom: -250px;
  right: -250px;

  background: #8b5cf6;

  filter: blur(180px);

  opacity: 0.18;

  z-index: -1;
}

section {
  padding: 100px 10%;
}
</style>
