<template>
  <div
    class="max-w-xl mx-auto mt-12 p-8 bg-gray-50 rounded-xl shadow text-center"
  >
    <h1 class="text-3xl font-bold mb-4">Welcome to KSA Izegem Nuxt App!</h1>
    <div>
      <span class="block mb-2">This page tests:</span>
      <ul class="list-disc list-inside text-left mx-auto inline-block">
        <li>ESLint (check your code quality in the editor)</li>
        <li
          >Nuxt Fonts:
          <span class="font-sans" style="font-family: 'Roboto', sans-serif"
            >This is Roboto font</span
          ></li
        >
        <li>Nuxt Icon: <Icon name="mdi:home" /></li>
        <li
          >Nuxt Image:
          <NuxtImg
            src="https://github.com/nuxt/fonts/assets/904724/75121716-05fd-459b-9223-42eb9dc8646f"
            width="48"
            height="48"
            alt="Nuxt Image test"
            class="inline align-middle ml-2"
        /></li>
      </ul>
    </div>
  </div>
</template>
