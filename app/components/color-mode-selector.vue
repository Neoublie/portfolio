<template>
  <div class="flex space-x-2 items-center">
    <div class="text-gray-500 text-xs" v-if="showNextModeLabel">Change to {{ nextMode }}</div>
    <button @click.prevent="toggleMode" @mouseenter="showNextModeLabel = true" @mouseleave="showNextModeLabel = false"
      class="hover:bg-gray-300 dark:hover:bg-gray-600 px-2 py-1 text-gray-500">{{
        nextModeIcon }} </button>
  </div>
</template>

<script lang="ts" setup>
const showNextModeLabel = ref(false)
const colorMode = useColorMode()

const modes = ['system', 'light', 'dark']

const nextModeIcons = {
  system: '🌓',
  light: '🌕',
  dark: '🌑'
}

const nextMode = computed(() => {
  const currentIndex = modes.indexOf(colorMode.preference)
  const nextIndex = (currentIndex + 1) % modes.length
  return modes[nextIndex]
})

const toggleMode = () => {
  colorMode.preference = nextMode.value
}

const nextModeIcon = computed(() => nextModeIcons[nextMode.value])

</script>