<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()

const { locale } = useI18n()

function setLocale(lang: string) {
  locale.value = lang
}
</script>

<template>
    <div class="w-32 p-4">
      <nav class="flex flex-col fixed space-y-2 w-1/18">
        <a href="#about" class="hover:underline text-sm">{{ t("navbar.about") }}</a>
        <a href="#projects" class="hover:underline text-sm">{{ t("navbar.projects") }}</a>
        <a href="#skills" class="hover:underline text-sm">{{ t("navbar.skills") }}</a>
        <br />
        <div class="text-sm">
    <a href="#" @click.prevent="setLocale('en')" :class="{ 'font-semibold': locale === 'en' }">ENG</a>
    |
    <a href="#" @click.prevent="setLocale('ja')" :class="{ 'font-semibold': locale === 'ja' }">JP</a>
  </div>
      </nav>
    </div>
</template>