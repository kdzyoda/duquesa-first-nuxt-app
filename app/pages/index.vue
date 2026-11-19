<script setup lang="ts">
useHead({
  title: 'Home',
  meta: [
    {
      name: 'description',
      content: 'Personal Profile Page - Khizha Rhizhane C. Duquesa'
    }
  ]
})
</script>

<template>
  <div>
    <section class="mx-auto grid min-h-[75vh] max-w-6xl items-center gap-12 px-6 py-16 lg:grid-cols-2 lg:px-8">
      <div>
        <div class="mb-7 inline-flex items-center gap-3 rounded-full border border-emerald-500/30 bg-emerald-500/10 px-4 py-2 text-xs font-semibold uppercase tracking-widest text-emerald-700 dark:text-emerald-400">
          <span class="h-2 w-2 rounded-full bg-emerald-500"></span>
          Welcome to khizha.dev personal profile page
        </div>

        <p class="mb-4 font-mono text-sm font-medium text-emerald-600 dark:text-emerald-400">
          01 / INTRODUCTION
        </p>

        <h1 class="mb-6 text-5xl font-black leading-tight tracking-tight sm:text-6xl">
          Hi, I'm
          <span class="text-emerald-600 dark:text-emerald-400">
            Khizha.
          </span>
        </h1>

        <h2 class="mb-6 text-xl font-medium text-slate-700 sm:text-2xl dark:text-slate-200">
          IT Student. Developer. Creator.
        </h2>

        <p class="max-w-xl text-base leading-8 text-slate-600 dark:text-slate-400">
          I'm Khizha Rhizhane C. Duquesa, a Bachelor of
          Science in Information Technology student at
          Caraga State University. I enjoy programming,
          building web applications, and exploring modern
          technologies that solve real-world problems.
        </p>

        <div class="mt-9 flex flex-wrap gap-3">
          <NuxtLink
            to="/profile"
            class="rounded-xl bg-emerald-600 px-7 py-3 font-semibold text-white transition hover:bg-emerald-700 dark:bg-emerald-400 dark:text-slate-950 dark:hover:bg-emerald-300"
          >
            Explore My Profile →
          </NuxtLink>

          <a
            href="https://github.com/kdzyoda"
            target="_blank"
            rel="noopener noreferrer"
            class="rounded-xl border border-slate-300 px-7 py-3 font-semibold transition hover:border-emerald-500 dark:border-white/20"
          >
            GitHub
          </a>
        </div>
      </div>

      <div class="mx-auto w-full max-w-md">
        <div class="overflow-hidden rounded-2xl border border-slate-200 bg-white shadow-xl dark:border-white/10 dark:bg-[#111C30]">
          <div class="flex items-center gap-2 border-b border-slate-200 px-5 py-4 dark:border-white/10">
            <span class="h-3 w-3 rounded-full bg-red-400"></span>
            <span class="h-3 w-3 rounded-full bg-amber-400"></span>
            <span class="h-3 w-3 rounded-full bg-emerald-400"></span>

            <span class="ml-3 font-mono text-xs text-slate-500 dark:text-slate-400">
              profile@khizha:~
            </span>
          </div>

          <div class="p-8 text-center">
            <img
              src="/profile.jpg"
              alt="Khizha Duquesa"
              class="mx-auto mb-6 h-44 w-44 rounded-2xl border-4 border-emerald-500/30 object-cover"
            />

            <h3 class="text-2xl font-bold">
              Khizha Rhizhane C. Duquesa
            </h3>

            <p class="mt-2 text-sm text-slate-500 dark:text-slate-400">
              III - BS Information Technology
            </p>

            <div class="mt-7 rounded-xl bg-slate-100 p-5 text-left font-mono text-xs leading-7 dark:bg-[#0B1120]">
              <p class="text-emerald-600 dark:text-emerald-400">
                $ student --status loaded!
              </p>
              <p class="text-slate-600 dark:text-slate-300">
                ✓ University: Caraga State University Main Campus
              </p>
              <p class="text-slate-600 dark:text-slate-300">
                ✓ Department: College of Computing & Information Sciences
              </p>
              <p class="text-slate-600 dark:text-slate-300">
                ✓ Course: BS Information Technology
              </p>
              <p class="text-emerald-600 dark:text-emerald-400">
                ✓ Status: Learning & Exploring_
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="border-t border-slate-200 bg-white/50 py-12 dark:border-white/10 dark:bg-white/[0.02]">
      <div class="mx-auto max-w-6xl px-6 lg:px-8">
        <p class="mb-6 text-center font-mono text-xs uppercase tracking-widest text-slate-500 dark:text-slate-400">
          Technologies I'm exploring
        </p>

        <div class="flex flex-wrap justify-center gap-3">
          <span
            v-for="tech in [
                'HTML & CSS',
                'TypeScript',
                'JavaScript',
                'PHP',
                'Laravel',
                'C',
                'Python',
                'Lua',
                'Vue.js',
                'Nuxt.js',
                'React',
                'MongoDB',
                'MySQL',
                'PostgreSQL',
                'Git',
                'UI/UX Fundamentals',
                'Adaptability',
                'Problem Solving',
                'AI Integration'
            ]"
            :key="tech"
            class="rounded-lg border border-slate-200 bg-white px-4 py-2 text-sm font-medium dark:border-white/10 dark:bg-white/5"
          >
            {{ tech }}
          </span>
        </div>
      </div>
    </section>
  </div>
</template>
