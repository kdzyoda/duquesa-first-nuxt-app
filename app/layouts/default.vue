<template>
  <div class="flex min-h-screen flex-col bg-[#F3F6FA] text-slate-900 transition-colors duration-200 dark:bg-[#0B1120] dark:text-white">
    <AppHeader />

    <main class="flex-1">
      <slot />
    </main>

    <footer class="border-t border-slate-200 px-6 py-7 dark:border-white/10">
      <div class="mx-auto flex max-w-6xl flex-col items-center justify-between gap-2 text-center text-sm text-slate-500 sm:flex-row dark:text-slate-400">
        <p>© 2026 Khizha Duquesa. All rights reserved.</p>
        <p>Built with Nuxt.js + Tailwind CSS</p>
      </div>
    </footer>
  </div>
</template>
