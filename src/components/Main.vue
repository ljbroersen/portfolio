<script setup lang="ts">
import AboutMeCard from "./AboutMeCard.vue";
import Footer from "./Footer.vue";
// import IntroductionCard from "./IntroductionCard.vue"
import ProjectsCard from "./ProjectsCard.vue";
import SkillsCard from "./SkillsCard.vue";
</script>

<template>
  <div class="min-h-screen flex justify-center bg-[rgb(var(--color-bg-primary))]">
    <div class="w-1/2 bg-[rgb(var(--color-bg-secondary))]">
      <!-- <IntroductionCard /> -->
      <AboutMeCard />
      <ProjectsCard />
      <SkillsCard />
      <Footer />
     </div>
  </div>
</template>
