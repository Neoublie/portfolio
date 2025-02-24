<template>
  <div class="container mx-auto max-w-2xl">
    <header class="flex justify-between items-center mt-5">
      <div class="flex items-center space-x-12">
        <div>
          <NuxtLink to="/" class="text-xl font-semibold p-2 hover:bg-gray-200">
            Graham Griffin
          </NuxtLink>
        </div>
        <Menu />
      </div>
      <ClientOnly>
        <color-mode-selector />
      </ClientOnly>
    </header>

    <main class="p-2 mt-10">
      <slot />
    </main>

    <footer class="flex justify-between items-center text-center mt-10">
      <p>&copy; 2021 Graham Griffin</p>
      <p>Dragontech Developments Limted</p>
    </footer>
  </div>
</template>

<script lang="ts" setup>
useHead({
  titleTemplate: '%s - Graham Griffin',
  link: [
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com'
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Roboto&display=swap'
    }
  ]
})

</script>

<style>
body {
  font-family: 'Roboto', sans-serif;
}

body {
  @apply bg-white dark:bg-gray-900 text-gray-800 dark:text-white
}
</style>
