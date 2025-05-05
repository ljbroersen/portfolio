<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
    <div class="w-30 p-4">
      <nav class="flex flex-col fixed space-y-2 w-1/16">
        <a href="#about" class="hover:underline text-sm">{{ t("navbar.about") }}</a>
        <a href="#projects" class="hover:underline text-sm">{{ t("navbar.projects") }}</a>
        <a href="#skills" class="hover:underline text-sm">{{ t("navbar.skills") }}</a>
      </nav>
    </div>
</template>