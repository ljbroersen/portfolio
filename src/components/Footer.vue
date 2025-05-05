<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
        <div class="border-t-0 border-b border-[rgb(var(--color-text-base))] 
            lg:border-l lg:border-r 
            p-4 lg:p-8">
      <div class="text-center">
        <p>{{ t('footer.footer_text') }}</p>
      </div>
    </div>
  </template>