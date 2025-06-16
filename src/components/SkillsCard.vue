<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
        <div class="border-t-0 border-b border-[rgb(var(--color-text-base))] 
            lg:border-l lg:border-r 
            p-4 lg:p-8">
      <div class="p-8">
        <h1 class="text-3xl font-bold text-[rgb(var(--color-primary))]">{{ t("skills.heading") }}</h1>
        <div class="mt-5">
            <table class="table-auto w-full">
      <tbody>
        <tr>
          <td class="px-4 py-2">
            <h2 class="text-2xl font-bold text-[rgb(var(--color-primary))]">{{ t("skills.subheading_languages") }}</h2>
            <p>{{ t("skills.language_skills") }}</p>
        </td>
          <td class="px-4 py-2">
            <h2 class="text-2xl font-bold text-[rgb(var(--color-primary))]">{{ t("skills.subheading_frameworks") }}</h2>
            <p>{{ t("skills.frameworks_skills") }}</p>
          </td>
        </tr>
        <tr>
          <td class="px-4 py-2">
            <h2 class="text-2xl font-bold text-[rgb(var(--color-primary))]">{{ t("skills.subheading_styling_ui") }}</h2>
            <p>{{ t("skills.styling_ui_skills") }}</p>
          </td>
          <td class="px-4 py-2">
            <h2 class="text-2xl font-bold text-[rgb(var(--color-primary))]">{{ t("skills.subheading_testing_frameworks") }}</h2>
            <p>{{ t("skills.testing_skills") }}</p>
          </td>
        </tr>
         <tr>
          <td class="px-4 py-2">
            <h2 class="text-2xl font-bold text-[rgb(var(--color-primary))]">{{ t("skills.subheading_tools_devops") }}</h2>
            <p>{{ t("skills.tools_devops_skills") }}</p>
          </td>
          </tr>
      </tbody>
    </table>
        </div>
      </div>
    </div>
  </template>