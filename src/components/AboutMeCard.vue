<template>
    <div class="border-t-0 border-b border-[rgb(var(--color-text-base))] 
            lg:border-l lg:border-r 
            p-4 lg:p-8">
      <div class="flex flex-col p-8 xl:flex-row xl:justify-start ">
        <div class="w-full sm:w-4/5 md:w-3/4 lg:w-1/2">
        <h1 class="text-3xl font-bold text-[rgb(var(--color-primary))]">My name is Lisa Broersen, a Full-stack Engineer based in Yokohama, Japan.</h1>
        <p>Being able to work on both the frontend and the backend, my speciality lies in <b>JavaScript/TypeScript</b>, <b>React</b> and <b>Node.js</b>.</p>
        <br />
        <p>With my work and skills, I want to make a difference and help people</p>
    </div>
    <div class="flex flex-col w-full xl:w-1/2 pt-8 xl:pt-0 xl:ml-24">
        <!-- <div class="w-[300px] h-[300px] bg-[rgb(var(--color-secondary))] flex justify-center items-center">
        <span class="text-white">Image</span>
      </div> -->
      <img src="../assets/photo_self_300px.png" width="300px" height="300px">
      <div class="flex flex-col mt-5 justify-between">
          <div class="flex flex-row"><img src="../assets/github_logo.svg" alt="GitHub Logo" class="mb-3 mr-3"><a href="https://github.com/ljbroersen" aria-label="Link to GitHub profile">Follow on GitHub</a></div>
          <div class="flex flex-row"><img src="../assets/linkedin_logo.svg" alt="LinkedIn Logo" class="mb-3 mr-3"><a href="https://www.linkedin.com/in/lisa-broersen/" aria-label="Link to LinkedIn profile">Follow on LinkedIn</a></div>
          <div class="flex flex-row"><img src="../assets/email_logo.svg" alt="" class="mb-3 mr-3" width="30px" height="30px"><a href="mailto:lj.broersen@gmail.com" aria-label="">lj.broersen@gmail.com</a></div>
        </div>
    </div>
      </div>
    </div>
  </template>