<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()

console.log("AboutMeCard loaded")
</script>

<template>
    <div class="border-t-0 border-b border-[rgb(var(--color-text-base))] 
            lg:border-l lg:border-r 
            p-4 lg:p-8">
      <div class="flex flex-col p-8 xl:flex-row xl:justify-start ">
        <div class="w-full sm:w-4/5 md:w-3/4 lg:w-1/2">
        <h1 class="text-3xl font-bold text-[rgb(var(--color-primary))]">{{ t("about.heading") }}</h1>
        <p>{{ t("about.description") }}</p>
        <br />
        <p>{{ t("about.description_two") }}</p>
    </div>
    <div class="flex flex-col w-full xl:w-1/2 pt-8 xl:pt-0 xl:ml-24">
      <img src="../assets/photo_self_300px.png" width="300px" height="300px">
      <div class="flex flex-col mt-5 justify-between">
          <div class="flex flex-row"><img src="../assets/github_logo.svg" alt="GitHub Logo" class="mb-3 mr-3"><a href="https://github.com/ljbroersen" aria-label="Link to GitHub profile">{{ t("about.github_link") }}</a></div>
          <div class="flex flex-row"><img src="../assets/linkedin_logo.svg" alt="LinkedIn Logo" class="mb-3 mr-3"><a href="https://www.linkedin.com/in/lisa-broersen/" aria-label="Link to LinkedIn profile">{{ t("about.linkedin_link") }}</a></div>
          <div class="flex flex-row"><img src="../assets/email_logo.svg" alt="" class="mb-3 mr-3" width="30px" height="30px"><a href="mailto:lj.broersen@gmail.com" aria-label="">{{ t("about.email_link") }}</a></div>
        </div>
    </div>
      </div>
    </div>
  </template>