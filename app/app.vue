<script setup lang="ts">
  // Global SEO configuration
  useHead({
    htmlAttrs: {
      lang: 'nl-BE',
    },
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { name: 'format-detection', content: 'telephone=no' },
      { name: 'author', content: 'KSA Izegem' },
      { name: 'robots', content: 'index,follow' },
      { name: 'googlebot', content: 'index,follow' },
      { property: 'og:site_name', content: 'KSA Izegem' },
      { property: 'og:locale', content: 'nl_BE' },
      { name: 'twitter:site', content: '@ksaizegem' },
      { name: 'theme-color', content: '#ffffff' },
    ],
  });
</script>

<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<style>
  h1,
  h2 {
    font-family: 'Patrick Hand', sans-serif;
    font-weight: 600;
  }

  * {
    font-family: 'Nunito', sans-serif;
    font-weight: 200;
  }

  a {
    font-family: 'Nunito', sans-serif;
  }
</style>
