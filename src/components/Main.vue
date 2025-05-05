<script setup lang="ts">
import AboutMeCard from "./AboutMeCard.vue";
import Footer from "./Footer.vue";
import Navbar from "./Navbar.vue";
import ProjectsCard from "./ProjectsCard.vue";
import SkillsCard from "./SkillsCard.vue";
</script>

<template>
  <div class="min-h-screen flex flex-col xl:flex-row justify-center bg-[rgb(var(--color-bg-primary))] text-[rgb(var(--color-text-base))]">
    <Navbar />
    <div class="w-full max-w-5xl bg-[rgb(var(--color-bg-secondary))] rounded-lg shadow">
      <section id="about">
        <AboutMeCard />
      </section>
      <section id="projects">
        <ProjectsCard />
      </section>
      <section id="skills">
        <SkillsCard />
      </section>
      <section id="footer">
        <Footer />
      </section>
    </div>
  </div>
</template>
