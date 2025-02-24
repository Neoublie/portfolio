<template>
  <div>
    <h1>Hello World</h1>
  </div>
</template>

<script lang="ts" setup>
useSeoMeta({
  title: 'Dragontech Developments',
  description: '[description]',
  ogTitle: 'Dragontech Developments',
  ogDescription: 'Dragontech Developments Portfolio',
  ogImage: '[og:image]',
  ogUrl: '[og:url]',
  twitterTitle: 'Dragontech Developments',
  twitterDescription: 'Dragontech Developments Portfolio',
  twitterImage: '[twitter:image]',
  twitterCard: 'summary'
})

useHead({
  htmlAttrs: {
    lang: 'en'
  },
  link: [
    {
      rel: 'icon',
      type: 'image/png',
      href: '/favicon.png'
    }
  ]
})

</script>

<style></style>