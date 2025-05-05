<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
        <div class="border-t-0 border-b border-[rgb(var(--color-text-base))] 
            lg:border-l lg:border-r 
            p-4 lg:p-8">
      <div class="p-8">
        <h1 class="text-3xl font-bold text-[rgb(var(--color-primary))]">{{ t('projects.heading')}}</h1>
        <h2 class="text-2xl font-bold">{{ t('projects.subheading_one')}}</h2>
        <div class="flex flex-col mt-5">
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="https://github.com/vitaeaggregate/main/raw/dev/frontend/src/lib/Logo.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/vitaeaggregate/main"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))]">{{ t('projects.project_one_title')}}</h2></a>
              <p>{{ t('projects.project_one_description')}}</p>
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
              <a href="https://github.com/builders-weekend-tradex/tradex-frontend"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))]">{{ t('projects.project_two_title')}}</h2></a>
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
            </div>
        </div>
        <h2 class="text-2xl font-bold">{{ t('projects.subheading_two')}}</h2>
        <div class="flex flex-col mt-5">
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="../assets/findadoc_heart-circle.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/ourjapanlife/findadoc-web"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))]">{{ t('projects.project_three_title')}}</h2></a>
              <p>{{ t('projects.project_three_description')}}</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">{{ t('projects.tech_heading')}}</h3>
              <p><b>{{ t('projects.tech_frontend')}}:</b> {{ t('projects.project_three_tech_frontend')}}</p>
              <p><b>{{ t('projects.tech_other')}}:</b> {{ t('projects.project_three_tech_other')}}</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">{{ t('projects.tasks_heading')}}</h3>
                <li>{{ t('projects.project_three_task_one')}}</li>
            </div>
        </div>
      </div>
    </div>
  </template>