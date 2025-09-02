<template>
  <header class="bg-white shadow-sm fixed top-0 inset-x-0 z-50">
    <nav
      class="max-w-5xl w-full mx-auto flex items-center justify-between py-4 px-4"
    >
      <!-- Logo -->
      <NuxtLink to="/" class="flex items-center transition hover:scale-95">
        <NuxtImg src="/logo.png" alt="KSA Izegem" class="h-10 w-auto" />
      </NuxtLink>

      <!-- Menu -->
      <ul
        class="hidden md:flex items-center space-x-6 font-medium translate-y-1"
      >
        <li class="hover:border-b border-black pb-1">
          <NuxtLink to="/leeftijdsgroepen" class="flex items-center gap-1"
            >Leeftijdsgroepen</NuxtLink
          >
        </li>
        <li class="hover:border-b border-black pb-1">
          <NuxtLink to="/contact" class="flex items-center gap-1"
            >Contact</NuxtLink
          >
        </li>
        <li class="hover:border-b border-black pb-1">
          <NuxtLink
            to="https://thunderball.ksaizegem.be"
            target="_blank"
            class="flex items-center gap-1"
          >
            Thunderball
            <Icon name="i-heroicons-arrow-top-right-on-square-20-solid" />
          </NuxtLink>
        </li>
        <li class="hover:border-b border-black pb-1">
          <NuxtLink
            to="https://shop.ksaizegem.be"
            target="_blank"
            class="flex items-center gap-1"
          >
            Webshops
            <Icon name="i-heroicons-arrow-top-right-on-square-20-solid" />
          </NuxtLink>
        </li>
        <!-- Button -->
        <li>
          <NuxtLink
            to="https://shop.ksaizegem.be/tokshop"
            target="_blank"
            class="ml-4 px-4 py-2 -translate-y-1 rounded-full border-2 border-orange-500 text-orange-500 hover:bg-orange-600 hover:text-white transition flex items-center gap-1"
          >
            Inschrijven
            <Icon name="i-heroicons-arrow-top-right-on-square-20-solid" />
          </NuxtLink>
        </li>
      </ul>
    </nav>
  </header>
</template>
