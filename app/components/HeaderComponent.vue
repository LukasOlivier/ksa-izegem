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
        <li class="hover:border-b border-black pb-1">
          <NuxtLink to="/" class="flex items-center gap-1">Home</NuxtLink>
        </li>
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

      <!-- Mobile Menu Button -->
      <button
        class="md:hidden flex items-center justify-center w-10 h-10 rounded-lg hover:bg-gray-100 transition-colors"
        :aria-expanded="isMenuOpen"
        aria-label="Toggle menu"
        @click="isMenuOpen = !isMenuOpen"
      >
        <Icon
          :name="isMenuOpen ? 'i-heroicons-x-mark' : 'i-heroicons-bars-3'"
          class="w-6 h-6"
        />
      </button>
    </nav>

    <!-- Mobile Menu Overlay -->
    <div
      v-if="isMenuOpen"
      class="md:hidden fixed inset-0 top-[72px] bg-black bg-opacity-50 z-40"
      @click="isMenuOpen = false"
    />

    <!-- Mobile Menu -->
    <div
      v-if="isMenuOpen"
      class="md:hidden fixed top-[72px] left-0 right-0 bg-white shadow-lg z-50 border-t border-gray-200"
    >
      <ul class="py-2">
        <li>
          <NuxtLink
            to="/"
            class="flex items-center px-6 py-3 hover:bg-gray-50 transition-colors"
            @click="closeMenu"
          >
            Home
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            to="/leeftijdsgroepen"
            class="flex items-center px-6 py-3 hover:bg-gray-50 transition-colors"
            @click="closeMenu"
          >
            Leeftijdsgroepen
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            to="/contact"
            class="flex items-center px-6 py-3 hover:bg-gray-50 transition-colors"
            @click="closeMenu"
          >
            Contact
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            to="https://thunderball.ksaizegem.be"
            target="_blank"
            class="flex items-center gap-2 px-6 py-3 hover:bg-gray-50 transition-colors"
            @click="closeMenu"
          >
            Thunderball
            <Icon
              name="i-heroicons-arrow-top-right-on-square-20-solid"
              class="w-4 h-4"
            />
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            to="https://shop.ksaizegem.be"
            target="_blank"
            class="flex items-center gap-2 px-6 py-3 hover:bg-gray-50 transition-colors"
            @click="closeMenu"
          >
            Webshops
            <Icon
              name="i-heroicons-arrow-top-right-on-square-20-solid"
              class="w-4 h-4"
            />
          </NuxtLink>
        </li>
        <li class="border-t border-gray-200 mt-2 pt-2">
          <NuxtLink
            to="https://shop.ksaizegem.be/tokshop"
            target="_blank"
            class="flex items-center justify-center gap-2 mx-6 my-3 px-4 py-3 rounded-full border-2 border-orange-500 text-orange-500 hover:bg-orange-600 hover:text-white transition"
            @click="closeMenu"
          >
            Inschrijven
            <Icon
              name="i-heroicons-arrow-top-right-on-square-20-solid"
              class="w-4 h-4"
            />
          </NuxtLink>
        </li>
      </ul>
    </div>
  </header>
</template>

<script setup>
  const isMenuOpen = ref(false);

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
