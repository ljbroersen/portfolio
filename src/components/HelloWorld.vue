<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <div class="min-h-screen flex items-center justify-center bg-[rgb(var(--color-bg-primary))]">
    <div class="w-1/2 p-6 bg-[rgb(var(--color-bg-secondary))] rounded-lg shadow text-center flex flex-col items-center">
      <h1 class="text-3xl font-bold text-[rgb(var(--color-primary))]">{{ msg }}</h1>

      <div class="card mt-4">
        <button 
          type="button" 
          @click="count++"
          class="px-4 py-2 mt-2 bg-[rgb(var(--color-primary))] text-[rgb(var(--color-primary-inverted))] rounded hover:bg-[rgb(var(--color-primary-hover))] transition"
        >
          count is {{ count }}
        </button>
        <p class="mt-2 text-sm text-[rgb(var(--color-text-muted))]">
          Edit <code>components/HelloWorld.vue</code> to test HMR
        </p>
      </div>

      <div class="mt-4 text-sm">
        <p>
          Check out
          <a 
            href="https://vuejs.org/guide/quick-start.html#local" 
            target="_blank"
            class="text-[rgb(var(--color-secondary))] underline hover:text-[rgb(var(--color-secondary-hover))]"
          >create-vue</a
          >, the official Vue + Vite starter
        </p>
        <p>
          Learn more about IDE Support for Vue in the
          <a 
            href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support" 
            target="_blank"
            class="text-[rgb(var(--color-secondary))] underline hover:text-[rgb(var(--color-secondary-hover))]"
          >Vue Docs Scaling up Guide</a
          >.
        </p>
      </div>

      <p class="read-the-docs mt-6 text-[rgb(var(--color-text-muted))]">
        Click on the Vite and Vue logos to learn more
      </p>
    </div>
  </div>
</template>
