<script setup lang="ts">
import { useI18n } from "vue-i18n";
import { defineProps, defineEmits } from "vue";
import { ref } from "vue";

const { show } = defineProps<{ show: boolean }>();
const emit = defineEmits<{ (e: "close"): void }>();

import submissionOverview from "../../../assets/findadocmoderationpanelredesign/submissionoverview.png";
import submissionOverviewExtras from "../../../assets/findadocmoderationpanelredesign/submissionoverviewextras.png";
import submissionOverviewMobile from "../../../assets/findadocmoderationpanelredesign/submissionoverview_mobile.png";
import submissionOverviewExtrasMobile from "../../../assets/findadocmoderationpanelredesign/submissionoverviewextras_mobile.png";

const slides = [
  { src: submissionOverview, alt: "Submission overview desktop design" },
  { src: submissionOverviewExtras, alt: "Submission overview extra components, buttons, features et cetera for desktop design" },
  { src: submissionOverviewMobile, alt: "Submission overview mobile design" },
  { src: submissionOverviewExtrasMobile, alt: "Submission overview navbar and navbar button for mobile design" },
];

const currentSlide = ref(0);

const nextSlide = () => {
  currentSlide.value = (currentSlide.value + 1) % slides.length;
};

const prevSlide = () => {
  currentSlide.value = (currentSlide.value - 1 + slides.length) % slides.length;
};

const { t } = useI18n();
</script>

<template>
  <div
    v-if="show"
    class="fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-70 p-4 sm:p-6"
    @click.self="emit('close')"
  >
    <div
      class="bg-[rgb(var(--color-bg-secondary))] rounded-xl w-full sm:w-[95%] max-w-3xl shadow-xl
             relative max-h-full sm:max-h-[90vh] overflow-y-auto flex flex-col"
    >
      <button
        @click="emit('close')"
        class="absolute top-3 right-4 text-[rgb(var(--color-tertiary))] text-2xl sm:text-3xl font-bold"
        aria-label="Close"
      >
        ×
      </button>

      <div class="p-4 sm:p-6 border-b border-gray-600 shrink-0">
        <h1 class="text-2xl sm:text-3xl font-bold text-[rgb(var(--color-primary))]">
          {{ t('projects.project_three_task_three_modal_title') }}
        </h1>
        <div class="flex flex-wrap gap-2 sm:gap-4 mt-1 sm:mt-2 text-md sm:text-lg text-gray-300">
          <span>
            ⏳ {{ t('projects.project_three_task_three_modal_status') }}
            <span class="bg-yellow-600 text-white px-2 py-0.5 rounded text-sm">
              {{ t('projects.project_three_task_three_modal_status_inprogress') }}
            </span>
          </span>
        </div>
      </div>

      <div class="p-4 sm:p-6 space-y-6 sm:space-y-8 overflow-y-auto flex-1 pb-6 sm:pb-8">
        <h2 class="text-base sm:text-lg font-semibold flex items-center">
          <span class="bg-gray-800 text-gray-200 px-2 sm:px-3 py-0.5 sm:py-1 rounded-full">
            {{ t('projects.project_three_task_three_modal_subheading_date_one') }}
          </span>
        </h2>

        <div class="bg-gray-800 rounded-lg p-3 sm:p-4 border-l-4 border-yellow-500">
          <div class="relative w-full h-[35vh] sm:h-[50vh] md:h-[55vh] mx-auto pb-6">
            <img
              :src="slides[currentSlide].src"
              :alt="slides[currentSlide].alt"
              class="rounded-lg shadow w-full h-full object-contain"
            />

            <button
              @click="prevSlide"
              class="absolute left-2 top-1/2 transform -translate-y-1/2
                     bg-black bg-opacity-40 text-white px-2 py-1 rounded-full hover:bg-opacity-70"
            >
              ‹
            </button>
            <button
              @click="nextSlide"
              class="absolute right-2 top-1/2 transform -translate-y-1/2
                     bg-black bg-opacity-40 text-white px-2 py-1 rounded-full hover:bg-opacity-70"
            >
              ›
            </button>

            <div class="absolute bottom-0 left-0 w-full flex justify-center mb-2 space-x-2">
              <span
                v-for="(_, index) in slides"
                :key="index"
                @click="currentSlide = index"
                class="w-3 h-3 rounded-full cursor-pointer"
                :class="index === currentSlide ? 'bg-[rgb(var(--color-primary))]' : 'bg-gray-500'"
              ></span>
            </div>
          </div>

          <p class="text-gray-200 mt-3 sm:mt-4 text-md sm:text-base mb-4">
            {{ t('projects.project_three_task_three_modal_subheading_date_one_explanation') }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
