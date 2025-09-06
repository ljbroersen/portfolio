<script setup lang="ts">
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
</script>

<template>
  <div
    v-if="show"
    class="fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-70"
    @click.self="emit('close')"
  >
    <div
      class="bg-[rgb(var(--color-bg-secondary))] rounded-xl w-[95%] max-w-3xl shadow-xl relative
             max-h-[90vh] overflow-hidden flex flex-col"
    >
      <button
        @click="emit('close')"
        class="absolute top-3 right-4 text-[rgb(var(--color-tertiary))] text-2xl font-bold"
        aria-label="Close"
      >
        ×
      </button>
      <div class="p-6 border-b border-gray-600 shrink-0">
        <h1 class="text-2xl font-bold text-[rgb(var(--color-primary))]">
          Moderation Panel Redesign Progress
        </h1>
        <div class="flex flex-wrap gap-4 mt-2 text-sm text-gray-300">
          <span>
            ⏳ Status:
            <span class="bg-yellow-600 text-white px-2 py-0.5 rounded">In Progress</span>
          </span>
        </div>
      </div>
      <div class="p-6 space-y-8 overflow-hidden flex-1">
        <div>
          <h2 class="text-lg font-semibold flex items-center">
            <span class="bg-gray-800 text-gray-200 px-3 py-1 rounded-full">
              July - August 2025
            </span>
          </h2>

          <div class="mt-4 space-y-6">
            <div class="bg-gray-800 rounded-lg p-4 border-l-4 border-yellow-500">
              <div class="relative w-full max-w-lg mx-auto h-[50vh]">
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
              <p class="text-gray-200 mt-4">
                The new design uses a more modern and visual layout, making information easier to read and understand at a glance. This way, users can find what they need faster and get a clearer overview without feeling overwhelmed.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>