<template>
  <footer class="bg-gray-50 py-8 mt-12">
    <div class="max-w-5xl w-full px-6 mx-auto">
      <!-- Main footer content -->
      <div class="flex flex-col md:flex-row items-center justify-between mb-6">
        <div class="text-center md:text-left mb-4 md:mb-0">
          <p class="font-semibold">KSA Izegem © 2025</p>
          <p class="text-gray-600 text-sm mt-1">
            Meensestraat 96<br />
            8870 Izegem
          </p>
        </div>
        <div class="flex space-x-4">
          <NuxtLink
            to="https://www.facebook.com/ksaizegem"
            target="_blank"
            aria-label="Facebook"
          >
            <Icon name="mdi:facebook" size="40" />
          </NuxtLink>
          <NuxtLink
            to="https://www.instagram.com/ksaizegem"
            target="_blank"
            aria-label="Instagram"
          >
            <Icon name="mdi:instagram" size="40" />
          </NuxtLink>
        </div>
      </div>

      <!-- Website credit -->
      <div class="border-t border-gray-200 pt-4 text-center">
        <p class="text-gray-500 text-sm">
          Website door
          <NuxtLink
            to="https://www.lukasolivier.be"
            target="_blank"
            class="text-orange-500 hover:text-orange-600 transition-colors"
          >
            Lukas Olivier
          </NuxtLink>
        </p>
      </div>
    </div>
  </footer>
</template>
