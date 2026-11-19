<script setup lang="ts">
type Theme = 'light' | 'dark'

const themeCookie = useCookie<Theme>('portfolio-theme', {
  default: () => 'dark',
  sameSite: 'lax',
  path: '/'
})

const theme = useState<Theme>('portfolio-theme-state', () =>
  themeCookie.value === 'light' ? 'light' : 'dark'
)

useHead({
  htmlAttrs: {
    class: computed(() => theme.value === 'dark' ? 'dark' : '')
  },
  titleTemplate: (title) =>
    title ? `${title} | Khizha.dev` : 'Khizha.dev'
})
</script>

<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
