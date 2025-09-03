<script setup lang="ts">
  // SEO configuration for homepage
  useSeoMeta({
    title: 'Home',
    description:
      'KSA Izegem biedt sinds 1927 plezier voor kinderen en jongeren met zaterdagnamiddagspelletjes, kampen, weekends en leuke activiteiten in Izegem.',
    ogTitle: 'KSA Izegem',
    ogDescription:
      'Ontdek KSA Izegem: een jeugdbeweging vol avontuur, vriendschap en plezier voor alle leeftijdsgroepen. Sinds 1927 actief in Izegem.',
    ogImage: '/index-hero.jpeg',
    ogImageAlt: 'KSA Izegem kinderen aan het spelen',
    ogType: 'website',
    ogUrl: 'https://ksaizegem.be',
    twitterCard: 'summary_large_image',
    twitterTitle: 'KSA Izegem',
    twitterDescription:
      'Ontdek KSA Izegem: een jeugdbeweging vol avontuur, vriendschap en plezier voor alle leeftijdsgroepen.',
    twitterImage: '/index-hero.jpeg',
    robots: 'index,follow',
    author: 'KSA Izegem',
    keywords:
      'KSA, Izegem, jeugdbeweging, kinderen, jongeren, kampen, activiteiten, katholiek, spelletjes, weekend, West-Vlaanderen',
  });

  // Canonical URL
  useHead({
    link: [{ rel: 'canonical', href: 'https://ksaizegem.be' }],
  });
</script>

<template>
  <div>
    <HeaderComponent />

    <!-- Hero Section -->
    <section
      class="relative h-[90vh] flex items-center justify-center text-center text-white"
    >
      <NuxtImg
        src="/index-hero.jpeg"
        alt="KSA kids"
        class="absolute inset-0 w-full h-full object-cover"
      />
      <div class="absolute inset-0 bg-black/40" />
      <div class="relative z-10">
        <h1 class="text-4xl md:text-7xl font-semibold mb-12">
          Spring mee in het verhaal van KSA
        </h1>
        <NuxtLink
          to="https://shop.ksaizegem.be/tokshop"
          target="_blank"
          class="bg-orange-600 font-semibold text-white px-6 py-3 rounded-full hover:bg-orange-700 transition"
        >
          Laten we ons inschrijven
        </NuxtLink>
      </div>
      <svg
        class="absolute left-0 w-full h-24 text-white block pointer-events-none -bottom-[1px]"
        viewBox="0 0 1440 320"
        preserveAspectRatio="none"
        aria-hidden="true"
      >
        <path
          d="M0,192C120,160,240,128,360,160C480,192,600,288,720,288C840,288,960,192,1080,160C1200,128,1320,160,1440,192L1440,320L0,320Z"
          fill="currentColor"
        />
      </svg>
    </section>

    <!-- Algemeen Section -->
    <section
      class="max-w-5xl mx-auto px-6 py-16 grid md:grid-cols-2 gap-10 items-center"
    >
      <div>
        <h2 class="text-5xl mb-6">Algemeen</h2>
        <p class="text-gray-700 mb-6">
          We heten je welkom op de site van KSA Izegem (Katholieke Studenten
          Actie). We zijn een jeugdbeweging die al van 1932 de Izegemse jeugd
          begeestert. Dit aan de hand van allerhande activiteiten die zich
          afspelen in de binnen- en buitenlucht. Uiteraard is dit niet het enige
          dat wij binnen KSA doen. Wij organiseren ook kampen, weekend, speciale
          activiteiten voor jong en oud, groot en klein!
        </p>
        <NuxtLink
          to="/contact"
          class="bg-ksa_blue text-white px-6 py-3 rounded-full hover:bg-blue-400 transition"
        >
          Ik heb vragen!
        </NuxtLink>
      </div>
      <div class="flex justify-center">
        <NuxtImg
          src="/index-algemeen.png"
          alt="Water fun"
          class="w-full max-w-md hidden md:block"
        />
      </div>
    </section>

    <!-- Leeftijdsgroepen Section -->
    <section id="leeftijdsgroepen" class="md:py-16 max-w-5xl mx-auto pb-16">
      <div class="px-6 grid gap-10 items-center">
        <div class="flex justify-center">
          <NuxtImg
            src="/index-leeftijdsgroepen.png"
            alt="KSA spelen"
            class="w-2/3 max-w-md"
          />
        </div>
        <div class="mx-auto w-full md:w-2/3">
          <h2 class="md:text-5xl text-4xl mb-6">Leeftijdsgroepen</h2>
          <p class="text-gray-700 mb-6">
            Vraag je je af hoe de KSA te werk gaat en waar je zoon terecht zal
            komen? Neem dan zeker eens een kijkje bij onze leeftijdsgroepen en
            ontmoet ons allemaal. Misschien vindt hij bij een van ons een
            verrassing!
          </p>
          <NuxtLink
            to="/leeftijdsgroepen"
            class="bg-ksa_blue text-white px-6 py-3 rounded-full hover:bg-blue-400 transition"
          >
            Bezoekje brengen
          </NuxtLink>
        </div>
      </div>
    </section>
    <FooterComponent />
  </div>
</template>
