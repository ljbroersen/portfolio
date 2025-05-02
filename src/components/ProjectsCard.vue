<template>
    <div class="border-[1px] border-[rgb(var(--color-primary))] border-t-[0px] p-8">
      <div class="p-8">
        <h1 class="text-3xl font-bold text-[rgb(var(--color-primary))]">Projects & Engagement</h1>
        <h2 class="text-2xl font-bold">Projects</h2>
        <div class="flex flex-col mt-5">
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="https://github.com/vitaeaggregate/main/raw/dev/frontend/src/lib/Logo.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/vitaeaggregate/main"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))]">Vitae Aggregate</h2></a>
              <p>A web-based resume management system built using Svelte, TypeScript, and Tailwind CSS. This application allows users to create, view, modify, and download resumes in ATS-compliant PDF format.</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">Tech stack</h3>
              <p><b>Frontend:</b> TypeScript, Svelte/SvelteKit</p>
              <p><b>Backend:</b> Python, Django, pytest</p>
              <p><b>Other:</b> Docker</p>
            </div>
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="https://github.com/builders-weekend-tradex/tradex-frontend/raw/main/src/assets/tradex-logo.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/builders-weekend-tradex/tradex-frontend"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))]">TradEx</h2></a>
              <p>TradEx is an application that provides users with real-time financial news and AI-powered insights. The platform integrates with external APIs to deliver the latest market updates and allows users to interact with an AI chatbot for personalized financial discussions.</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">Tech stack</h3>
              <p><b>Frontend:</b> TypeScript, React, Vitest</p>
              <p><b>Backend:</b> Python, FastAPI, pytest</p>
              <p><b>Other:</b> Text</p>
            </div>
        </div>
        <h2 class="text-2xl font-bold">Engagement</h2>
        <div class="flex flex-col mt-5">
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <div class="w-[75px] h-[75px] bg-[rgb(var(--color-secondary))] rounded-full flex justify-center items-center m-4"></div>
              <a href="https://github.com/ourjapanlife/findadoc-web"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))]">Find a Doc, Japan</h2></a>
              <p>Text</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">Tech stack</h3>
              <p><b>Frontend:</b> TypeScript, Vue.js, Nuxt, GraphQL, Cypress, Pinia</p>
              <p><b>Other:</b></p>
            </div>
        </div>
      </div>
    </div>
  </template>