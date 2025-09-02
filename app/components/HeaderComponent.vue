<template>
  <header class="bg-white shadow-sm fixed top-0 inset-x-0 z-50">
    <nav
      class="max-w-4xl w-full mx-auto flex items-center justify-between py-4 px-4"
    >
      <!-- Logo -->
      <NuxtLink to="/" class="flex items-center transition hover:scale-95">
        <NuxtImg src="/logo.png" alt="KSA Izegem" class="h-10 w-auto" />
      </NuxtLink>

      <!-- Menu -->
      <ul class="hidden md:flex items-center space-x-6 font-medium">
        <li>
          <NuxtLink
            to="#leeftijdsgroepen"
            class="hover:border-b border-black pb-1"
            >Leeftijdsgroepen</NuxtLink
          >
        </li>
        <li>
          <NuxtLink to="#contact" class="hover:border-b border-black pb-1"
            >Contact</NuxtLink
          >
        </li>
        <li>
          <NuxtLink to="#tokshop" class="hover:border-b border-black pb-1"
            >Tokshop</NuxtLink
          >
        </li>
        <!-- Button -->
        <NuxtLink
          to="#inschrijven"
          class="ml-4 px-4 py-2 rounded-full border-2 border-orange-500 text-orange-500 hover:bg-orange-600 hover:text-white transition"
        >
          Inschrijven
        </NuxtLink>
      </ul>
    </nav>
  </header>
</template>
