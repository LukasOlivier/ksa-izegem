<template>
  <header class="bg-white shadow-sm fixed top-0 inset-x-0 z-50">
    <nav
      class="max-w-5xl w-full mx-auto flex items-center justify-between py-4 px-4"
    >
      <!-- Logo -->
      <NuxtLink to="/" class="flex items-center transition hover:scale-95">
        <NuxtImg src="/logo.png" alt="KSA Izegem" class="h-10 w-auto" />
      </NuxtLink>

      <!-- Desktop Menu -->
      <ul
        class="hidden md:flex items-center space-x-6 font-medium translate-y-1"
      >
        <li
          v-for="navLink in navigationLinks"
          :key="navLink.url"
          class="hover:border-b border-black pb-1"
        >
          <NuxtLink :to="navLink.url" class="flex items-center gap-1">
            {{ navLink.title }}
          </NuxtLink>
        </li>
        <li
          v-for="externalLink in externalLinks"
          :key="externalLink.url"
          class="hover:border-b border-black pb-1"
        >
          <NuxtLink
            :to="externalLink.url"
            target="_blank"
            class="flex items-center gap-1"
          >
            {{ externalLink.title }}
            <Icon name="i-heroicons-arrow-top-right-on-square-20-solid" />
          </NuxtLink>
        </li>
        <!-- Special Button -->
        <li>
          <NuxtLink
            :to="specialButton.url"
            target="_blank"
            class="ml-4 px-4 py-2 -translate-y-1 rounded-full border-2 border-orange-500 text-orange-500 hover:bg-orange-600 hover:text-white transition flex items-center gap-1"
          >
            {{ specialButton.title }}
            <Icon name="i-heroicons-arrow-top-right-on-square-20-solid" />
          </NuxtLink>
        </li>
      </ul>

      <!-- Mobile Menu Button -->
      <button
        class="md:hidden flex items-center justify-center w-10 h-10 rounded-lg hover:bg-gray-100 transition-colors"
        :aria-expanded="isMenuOpen"
        aria-label="Toggle menu"
        @click="isMenuOpen = !isMenuOpen"
      >
        <Icon
          :name="isMenuOpen ? 'i-heroicons-x-mark' : 'i-heroicons-bars-3'"
          class="w-6 h-6 transition-transform duration-200 ease-in-out"
          :class="{ 'rotate-90': isMenuOpen }"
        />
      </button>
    </nav>

    <!-- Mobile Menu -->
    <Transition
      enter-active-class="transition-all duration-300 ease-out"
      enter-from-class="opacity-0 -translate-y-4"
      enter-to-class="opacity-100 translate-y-0"
      leave-active-class="transition-all duration-200 ease-in"
      leave-from-class="opacity-100 translate-y-0"
      leave-to-class="opacity-0 -translate-y-4"
    >
      <div
        v-if="isMenuOpen"
        class="md:hidden fixed top-[72px] left-0 right-0 bg-white shadow-lg z-50"
      >
        <ul class="py-2">
          <!-- Navigation Links -->
          <li
            v-for="(navLink, index) in navigationLinks"
            :key="navLink.url"
            class="transform transition-all duration-300 ease-out"
            :class="
              isMenuOpen
                ? 'translate-x-0 opacity-100'
                : 'translate-x-4 opacity-0'
            "
            :style="{ transitionDelay: isMenuOpen ? `${index * 50}ms` : '0ms' }"
          >
            <NuxtLink
              :to="navLink.url"
              class="flex items-center px-6 py-3 hover:bg-gray-50 transition-colors"
              @click="closeMenu"
            >
              {{ navLink.title }}
            </NuxtLink>
          </li>
          <!-- External Links -->
          <li
            v-for="(externalLink, index) in externalLinks"
            :key="externalLink.url"
            class="transform transition-all duration-300 ease-out"
            :class="
              isMenuOpen
                ? 'translate-x-0 opacity-100'
                : 'translate-x-4 opacity-0'
            "
            :style="{
              transitionDelay: isMenuOpen
                ? `${(navigationLinks.length + index) * 50}ms`
                : '0ms',
            }"
          >
            <NuxtLink
              :to="externalLink.url"
              target="_blank"
              class="flex items-center gap-2 px-6 py-3 hover:bg-gray-50 transition-colors"
              @click="closeMenu"
            >
              {{ externalLink.title }}
              <Icon
                name="i-heroicons-arrow-top-right-on-square-20-solid"
                class="w-4 h-4"
              />
            </NuxtLink>
          </li>
          <li
            class="border-t border-gray-200 mt-2 pt-2 transform transition-all duration-300 ease-out"
            :class="
              isMenuOpen
                ? 'translate-x-0 opacity-100'
                : 'translate-x-4 opacity-0'
            "
            :style="{
              transitionDelay: isMenuOpen
                ? `${(navigationLinks.length + externalLinks.length) * 50}ms`
                : '0ms',
            }"
          >
            <NuxtLink
              :to="specialButton.url"
              target="_blank"
              class="flex items-center justify-center gap-2 mx-6 my-3 px-4 py-3 rounded-full border-2 border-orange-500 text-orange-500 hover:bg-orange-600 hover:text-white transition"
              @click="closeMenu"
            >
              {{ specialButton.title }}
              <Icon
                name="i-heroicons-arrow-top-right-on-square-20-solid"
                class="w-4 h-4"
              />
            </NuxtLink>
          </li>
        </ul>
      </div>
    </Transition>
  </header>
</template>

<script setup>
  const isMenuOpen = ref(false);

  // Navigation links configuration
  const navigationLinks = [
    {
      title: 'Home',
      url: '/',
    },
    {
      title: 'Leeftijdsgroepen',
      url: '/leeftijdsgroepen',
    },
    {
      title: 'Contact',
      url: '/contact',
    },
  ];

  // External links configuration
  const externalLinks = [
    {
      title: 'Thunderball',
      url: 'https://thunderball.ksaizegem.be',
    },
    {
      title: 'Webshops',
      url: 'https://shop.ksaizegem.be',
    },
  ];

  // Special button configuration
  const specialButton = {
    title: 'Inschrijven',
    url: 'https://shop.ksaizegem.be/tokshop',
  };

  const closeMenu = () => {
    isMenuOpen.value = false;
  };

  // Close menu when route changes
  const route = useRoute();
  watch(
    () => route.path,
    () => {
      isMenuOpen.value = false;
    },
  );

  // Close menu on escape key
  onMounted(() => {
    const handleEscape = (event) => {
      if (event.key === 'Escape') {
        isMenuOpen.value = false;
      }
    };

    document.addEventListener('keydown', handleEscape);

    onUnmounted(() => {
      document.removeEventListener('keydown', handleEscape);
    });
  });
</script>
