<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { ref } from 'vue'

const showModal = ref(false)
const openVideoModal = () => (showModal.value = true)
const closeVideoModal = () => (showModal.value = false)

const { t } = useI18n()
</script>

<template>
        <div class="border-t-0 border-b border-[rgb(var(--color-text-base))] 
            lg:border-l lg:border-r 
            p-4 lg:p-8">
      <div class="p-8">
        <h1 class="text-3xl font-bold text-[rgb(var(--color-primary))]">{{ t('projects.heading')}}</h1>
        <p>{{ t('projects.name_project_link_explanation')}}</p>
        <h2 class="text-2xl font-bold">{{ t('projects.subheading_one')}}</h2>
        <div class="flex flex-col mt-5">
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="https://github.com/vitaeaggregate/main/raw/dev/frontend/src/lib/Logo.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/vitaeaggregate/main"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))] hover:text-[rgb(var(--color-primary))]">{{ t('projects.project_one_title')}}</h2></a>
              <p>{{ t('projects.project_one_description')}}</p>
              <button @click="openVideoModal" class="text-[rgb(var(--color-primary))] underline mt-2 cursor-pointer">
                {{ t('projects.demo_video_link')}}
              </button>
              <div
                v-if="showModal"
                class="fixed inset-0 z-50 flex items-center justify-center bg-[rgb(var(--color-bg-primary))] bg-opacity-60"
                @click.self="closeVideoModal"
              >
                <div
                  class="bg-[rgb(var(--color-bg-secondary))] rounded-lg w-[90%] max-w-sm shadow-xl relative pt-10 pb-4 px-4"
                >
                  <button
                    @click="closeVideoModal"
                    class="absolute top-2 right-2 text-[rgb(var(--color-tertiary))] text-2xl font-bold"
                    aria-label="Close"
                  >
                    ×
                  </button>
                  <video
                    controls
                    class="w-full rounded-md mt-2"
                    preload="metadata"
                  >
                    <source src="../assets/VA_mobile_demo.mp4" type="video/mp4" />
                    {{ t('projects.demo_video_not_visible')}}
                  </video>
                </div>
              </div>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">{{ t('projects.tech_heading')}}</h3>
              <p><b>{{ t('projects.tech_frontend')}}:</b> {{ t('projects.project_one_tech_frontend')}}</p>
              <p><b>{{ t('projects.tech_backend')}}:</b> {{ t('projects.project_one_tech_backend')}}</p>
              <p><b>{{ t('projects.tech_other')}}:</b> {{ t('projects.project_one_tech_other')}}</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">{{ t('projects.tasks_heading')}}</h3>
                <li>{{ t('projects.project_one_task_one')}}</li>
                <li>{{ t('projects.project_one_task_two')}}</li>
                <li>{{ t('projects.project_one_task_three')}}</li>
            </div>
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="https://github.com/builders-weekend-tradex/tradex-frontend/raw/main/src/assets/tradex-logo.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/builders-weekend-tradex/tradex-frontend"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))] hover:text-[rgb(var(--color-primary))]">{{ t('projects.project_two_title')}}</h2></a>
              <p>{{ t('projects.project_two_description')}}</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">{{ t('projects.tech_heading')}}</h3>
              <p><b>{{ t('projects.tech_frontend')}}:</b> {{ t('projects.project_two_tech_frontend')}}</p>
              <p><b>{{ t('projects.tech_backend')}}:</b> {{ t('projects.project_two_tech_backend')}}</p>
              <p><b>{{ t('projects.tech_other')}}:</b> {{ t('projects.project_two_tech_other')}}</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">{{ t('projects.tasks_heading')}}</h3>
                <li>{{ t('projects.project_two_task_one')}}</li>
                <li>{{ t('projects.project_two_task_two')}}</li>
                <li>{{ t('projects.project_two_task_three')}}</li>
                <li>{{ t('projects.project_two_task_four')}}</li>
            </div>
        </div>
        <h2 class="text-2xl font-bold">{{ t('projects.subheading_two')}}</h2>
        <div class="flex flex-col mt-5">
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="../assets/findadoc_heart-circle.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/ourjapanlife/findadoc-web"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))] hover:text-[rgb(var(--color-primary))]">{{ t('projects.project_three_title')}}</h2></a>
              <p>{{ t('projects.project_three_description')}}</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">{{ t('projects.tech_heading')}}</h3>
              <p><b>{{ t('projects.tech_frontend')}}:</b> {{ t('projects.project_three_tech_frontend')}}</p>
              <p><b>{{ t('projects.tech_other')}}:</b> {{ t('projects.project_three_tech_other')}}</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">{{ t('projects.tasks_heading')}}</h3>
                <li>{{ t('projects.project_three_task_one')}}</li>
                <li>{{ t('projects.project_three_task_two')}}</li>
                 <a href="https://github.com/ourjapanlife/findadoc-web/issues?q=author%3Aljbroersen" class="text-[rgb(var(--color-primary))] underline mt-2 cursor-pointer">{{ t('projects.github_link_contributions_project')}}</a>
            </div>
        </div>
      </div>
    </div>
  </template>