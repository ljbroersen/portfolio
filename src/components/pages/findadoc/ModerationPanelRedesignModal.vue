<script setup lang="ts">
import { defineProps, defineEmits } from "vue";

const { show } = defineProps<{ show: boolean }>();
const emit = defineEmits<{ (e: "close"): void }>();
</script>

<template>
  <div
    v-if="show"
    class="fixed inset-0 z-50 flex items-center justify-center bg-[rgb(var(--color-bg-primary))] bg-opacity-60"
    @click.self="emit('close')"
  >
    <div
      class="bg-[rgb(var(--color-bg-secondary))] rounded-lg w-[90%] max-w-lg shadow-xl relative pt-10 pb-4 px-4"
    >
      <button
        @click="emit('close')"
        class="absolute top-2 right-2 text-[rgb(var(--color-tertiary))] text-2xl font-bold"
        aria-label="Close"
      >
        ×
      </button>

      <h2 class="text-2xl font-bold mb-4">Moderation Panel Redesign</h2>
      <p class="mb-4">
        Work in progress. Please come back later.
      </p>
    </div>
  </div>
</template>
