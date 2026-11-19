
<script setup lang="ts">
useHead({
  title: 'Profile'
})

const skillCategories = [
  {
    title: 'Programming Languages',
    skills: [
      'C',
      'TypeScript',
      'JavaScript',
      'PHP',
      'Python',
      'Lua'
    ]
  },
  {
    title: 'Frameworks & Frontend',
    skills: [
      'HTML & CSS',
      'Laravel',
      'Vue.js',
      'Nuxt.js',
      'React'
    ]
  },
  {
    title: 'Databases & Development Tools',
    skills: [
      'MongoDB',
      'MySQL',
      'PostgreSQL',
      'Git'
    ]
  },
  {
    title: 'Other Skills & Interests',
    skills: [
      'UI/UX Fundamentals',
      'Adaptability',
      'Problem Solving',
      'AI Integration'
    ]
  }
]

const hobbies = [
  'Programming and building projects',
  'Playing video games',
  'Playing musical instruments',
  'Exploring new technologies'
]
</script>

<template>
  <section class="mx-auto max-w-5xl px-6 py-16 lg:px-8">
    <!-- Page Header -->
    <div class="mb-12">
      <p class="mb-4 font-mono text-sm text-emerald-600 dark:text-emerald-400">
        02 / STUDENT PROFILE
      </p>

      <h1 class="mb-4 text-4xl font-black tracking-tight sm:text-5xl">
        Behind the
        <span class="text-emerald-600 dark:text-emerald-400">
          code.
        </span>
      </h1>

      <p class="max-w-2xl leading-7 text-slate-600 dark:text-slate-400">
        A little more about who I am, what I'm learning,
        and what motivates me.
      </p>
    </div>

    <!-- Profile Cards -->
    <div class="grid gap-5 md:grid-cols-2">
      <!-- Personal Information -->
      <article
        class="rounded-2xl border border-slate-200 bg-white p-7 shadow-sm dark:border-white/10 dark:bg-[#111C30]"
      >
        <p class="mb-4 font-mono text-xs text-emerald-600 dark:text-emerald-400">
          01 / ABOUT ME
        </p>

        <h2 class="mb-6 text-2xl font-bold">
          Personal Information
        </h2>

        <div class="space-y-4 text-sm">
          <div>
            <p class="text-slate-500">Full Name</p>
            <p class="mt-1 font-medium">
              Khizha Rhizhane C. Duquesa
            </p>
          </div>

          <div>
            <p class="text-slate-500">Location</p>
            <p class="mt-1 font-medium">
              Butuan City, Philippines
            </p>
          </div>

          <div>
            <p class="text-slate-500">Field</p>
            <p class="mt-1 font-medium">
              Information Technology
            </p>
          </div>
        </div>
      </article>

      <!-- Educational Background -->
      <article
        class="rounded-2xl border border-slate-200 bg-white p-7 shadow-sm dark:border-white/10 dark:bg-[#111C30]"
      >
        <p class="mb-4 font-mono text-xs text-emerald-600 dark:text-emerald-400">
          02 / ACADEMICS
        </p>

        <h2 class="mb-6 text-2xl font-bold">
          Educational Background
        </h2>

        <p class="font-semibold">
          Caraga State University
        </p>

        <p class="mt-2 text-sm text-slate-600 dark:text-slate-400">
          Main Campus — Ampayon, Butuan City
        </p>

        <p class="mt-5 text-sm font-medium">
          Bachelor of Science in Information Technology
        </p>

        <p class="mt-2 text-sm text-slate-500">
          College of Computing and Information Sciences
        </p>
      </article>

      <!-- Skills and Interests -->
      <article
        class="rounded-2xl border border-slate-200 bg-white p-7 shadow-sm dark:border-white/10 dark:bg-[#111C30]"
      >
        <p class="mb-4 font-mono text-xs text-emerald-600 dark:text-emerald-400">
          03 / TECH STACK
        </p>

        <h2 class="mb-6 text-2xl font-bold">
          Skills & Interests
        </h2>

        <!-- Categorized Skills -->
        <div class="space-y-6">
          <div
            v-for="category in skillCategories"
            :key="category.title"
          >
            <h3
              class="mb-3 text-xs font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400"
            >
              {{ category.title }}
            </h3>

            <div class="flex flex-wrap gap-2">
              <span
                v-for="skill in category.skills"
                :key="skill"
                class="rounded-lg border border-emerald-500/20 bg-emerald-500/10 px-3 py-2 text-xs font-medium text-emerald-800 dark:text-emerald-300"
              >
                {{ skill }}
              </span>
            </div>
          </div>
        </div>

        <p class="mt-6 text-sm leading-7 text-slate-600 dark:text-slate-400">
          Interested in full-stack development,
          software engineering, modern web technologies,
          and AI-powered solutions.
        </p>
      </article>

      <!-- Hobbies -->
      <article
        class="rounded-2xl border border-slate-200 bg-white p-7 shadow-sm dark:border-white/10 dark:bg-[#111C30]"
      >
        <p class="mb-4 font-mono text-xs text-emerald-600 dark:text-emerald-400">
          04 / BEYOND THE SCREEN
        </p>

        <h2 class="mb-6 text-2xl font-bold">
          Hobbies
        </h2>

        <ul class="space-y-4">
          <li
            v-for="hobby in hobbies"
            :key="hobby"
            class="flex items-center gap-3 text-sm"
          >
            <span
              class="h-2 w-2 shrink-0 rounded-full bg-emerald-500"
            ></span>

            {{ hobby }}
          </li>
        </ul>
      </article>
    </div>

    <!-- Back Navigation -->
    <div class="mt-12 flex justify-center">
      <NuxtLink
        to="/"
        class="rounded-xl bg-emerald-600 px-7 py-3 font-semibold text-white transition hover:bg-emerald-700 dark:bg-emerald-400 dark:text-slate-950"
      >
        ← Back to Homepage
      </NuxtLink>
    </div>
  </section>
</template>
