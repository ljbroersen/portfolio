<template>
    <div class="border-[1px] border-[rgb(var(--color-primary))] border-t-[0px] p-8">
      <div class="p-8">
        <h1 class="text-3xl font-bold text-[rgb(var(--color-primary))]">Projects & Engagement</h1>
        <h2 class="text-2xl font-bold">Projects</h2>
        <div class="flex flex-col mt-5">
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="https://github.com/vitaeaggregate/main/raw/dev/frontend/src/lib/Logo.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/vitaeaggregate/main"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))]">Vitae Aggregate</h2></a>
              <p>Vitae Aggregate is a web-based resume management system built using Svelte, TypeScript, and Tailwind CSS. This application allows users to create, view, modify, and download resumes in ATS-compliant PDF format.</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">Tech stack</h3>
              <p><b>Frontend:</b> TypeScript, Svelte/SvelteKit, Tailwind CSS</p>
              <p><b>Backend:</b> Python, Django REST, pytest, PostgreSQL</p>
              <p><b>Other:</b> Docker, figma</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">Tasks</h3>
              <ul>
                <li>Drafted the database schema in a way that it could be dynamically used later.</li>
                <li>Set up the Models, Views and Routes with Python and the Django REST API framework and made sure the data could be retrieved from the PostgreSQL database.</li>
                <li>Converted figma mockups to a responsive mobile-first UI.</li>
              </ul>
            </div>
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="https://github.com/builders-weekend-tradex/tradex-frontend/raw/main/src/assets/tradex-logo.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/builders-weekend-tradex/tradex-frontend"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))]">TradEx</h2></a>
              <p>TradEx is an application that provides users with real-time financial news and AI-powered insights. The platform integrates with external APIs to deliver the latest market updates and allows users to interact with an AI chatbot for personalized financial discussions.</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">Tech stack</h3>
              <p><b>Frontend:</b> TypeScript, React, Tailwind CSS, Vitest</p>
              <p><b>Backend:</b> Python, FastAPI, pytest</p>
              <p><b>Other:</b> -</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">Tasks</h3>
              <ul>
                <li>Set up the backend, so that the charts and AI outputs could be rendered.</li>
                <li>Configured the API endpoints with FastAPI.</li>
                <li>Set up and configured testing with pytest and Vitest for both frontend and backend.</li>
              </ul>
            </div>
        </div>
        <h2 class="text-2xl font-bold">Engagement</h2>
        <div class="flex flex-col mt-5">
            <div class="w-full bg-[rgb(var(--color-bg-tertiary))] p-4 my-4">
              <img src="../assets/findadoc_heart-circle.png" width="75px" height="75px" class="m-4">
              <a href="https://github.com/ourjapanlife/findadoc-web"><h2 class="text-xl font-bold text-[rgb(var(--color-tertiary))]">Find a Doc, Japan</h2></a>
              <p>Find a Doc is an innovative online platform dedicated to enhancing healthcare accessibility for all individuals in Japan. Spearheaded by a diverse multinational team, the project fosters robust collaborations with both international communities and Japanese service providers and supporters.</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">Tech stack</h3>
              <p><b>Frontend:</b> TypeScript, Vue.js, Nuxt, Tailwind CSS, GraphQL, Cypress, Vitest, Pinia</p>
              <p><b>Other:</b> -</p>
              <br />
              <h3 class="text-lg text-[rgb(var(--color-tertiary))]">Tasks</h3>
              <ul>
                <li>Responsible for improving and implementing features, UX/UI, etc.</li>
              </ul>
            </div>
        </div>
      </div>
    </div>
  </template>