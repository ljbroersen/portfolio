<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()

const { locale } = useI18n()

function setLocale(lang: string) {
  locale.value = lang
}
</script>

<template>
  <div class="xl:hidden sticky top-0 z-50 bg-[rgb(var(--color-bg-primary))] p-4 border-b border-[rgb(var(--color-text-base))]">
    <nav class="flex justify-between items-center text-sm">
      <div class="flex space-x-4">
        <a href="#about" class="hover:underline">{{ t("navbar.about") }}</a>
        <a href="#projects" class="hover:underline">{{ t("navbar.projects") }}</a>
        <a href="#skills" class="hover:underline">{{ t("navbar.skills") }}</a>
      </div>
      <div class="text-sm">
        <a href="#" @click.prevent="setLocale('en')" :class="{ 'font-semibold': locale === 'en' }">ENG</a> |
        <a href="#" @click.prevent="setLocale('ja')" :class="{ 'font-semibold': locale === 'ja' }">JP</a>
      </div>
    </nav>
  </div>

  <div class="hidden xl:block w-32 p-4">
    <nav class="flex flex-col fixed space-y-2 text-sm w-1/18">
      <a href="#about" class="hover:underline">{{ t("navbar.about") }}</a>
      <a href="#projects" class="hover:underline">{{ t("navbar.projects") }}</a>
      <a href="#skills" class="hover:underline">{{ t("navbar.skills") }}</a>
      <br />
      <div>
        <a href="#" @click.prevent="setLocale('en')" :class="{ 'font-semibold': locale === 'en' }">ENG</a> |
        <a href="#" @click.prevent="setLocale('ja')" :class="{ 'font-semibold': locale === 'ja' }">JP</a>
      </div>
    </nav>
  </div>
</template>
