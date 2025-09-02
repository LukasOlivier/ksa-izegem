<template>
  <div>
    <HeaderComponent />

    <!-- Locatie Section -->
    <section class="px-6 mx-auto pb-20 mt-32 max-w-4xl">
      <h1 class="text-5xl font-extrabold mb-12 text-center">Locatie</h1>

      <div class="flex flex-col items-center gap-12">
        <!-- Map -->
        <div
          class="w-full max-w-[900px] h-[500px] rounded-2xl overflow-hidden shadow-2xl"
        >
          <iframe
            class="w-full h-full"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2533.354114646018!2d3.2022289769829917!3d50.913573771685316!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c33aeb8f3d5c19%3A0x5e6e4d8a0b8b41e!2sMeensestraat%2096%2C%208870%20Izegem!5e0!3m2!1snl!2sbe!4v1693664400000!5m2!1snl!2sbe"
            allowfullscreen
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          />
        </div>

        <!-- Address -->
        <p class="text-xl text-gray-700">Meensestraat 96 - 8870 Izegem</p>
      </div>
    </section>

    <!-- Onze Gegevens Section -->
    <section class="px-6 mx-auto py-20 max-w-4xl text-center">
      <h2 class="text-5xl font-extrabold mb-12">Onze gegevens</h2>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
        <!-- Kabouters -->
        <div>
          <NuxtImg
            src="/kabouters.png"
            alt="Kabouters"
            class="w-40 mx-auto mb-4"
          />
          <h3 class="text-xl font-semibold">Kabouters</h3>
          <p class="text-gray-600 mb-2">6-8 jaar (1e en 2e leerjaar)</p>
          <p class="flex items-center justify-center text-gray-700">
            <Icon name="mdi:email" class="text-orange-500 mr-2" />
            kabouters@ksaizegem.be
          </p>
        </div>

        <!-- Piepjongknapen -->
        <div>
          <NuxtImg
            src="/piepjongknapen.png"
            alt="Piejongknapen"
            class="w-40 mx-auto mb-4"
          />
          <h3 class="text-xl font-semibold">Piejongknapen</h3>
          <p class="text-gray-600 mb-2">8-10 jaar (3e en 4e leerjaar)</p>
          <p class="flex items-center justify-center text-gray-700">
            <Icon name="mdi:email" class="text-orange-500 mr-2" />
            piejongknapen@ksaizegem.be
          </p>
        </div>

        <!-- Jongknapen -->
        <div>
          <NuxtImg
            src="/jongknapen.png"
            alt="Jongknapen"
            class="w-40 mx-auto mb-4"
          />
          <h3 class="text-xl font-semibold">Jongknapen</h3>
          <p class="text-gray-600 mb-2">10-12 jaar (5e en 6e leerjaar)</p>
          <p class="flex items-center justify-center text-gray-700">
            <Icon name="mdi:email" class="text-orange-500 mr-2" />
            jongknapen@ksaizegem.be
          </p>
        </div>

        <!-- Knappen -->
        <div>
          <NuxtImg src="/knapen.png" alt="Knapen" class="w-40 mx-auto mb-4" />
          <h3 class="text-xl font-semibold">Knapen</h3>
          <p class="text-gray-600 mb-2">12-14 jaar (1e en 2e secundair)</p>
          <p class="flex items-center justify-center text-gray-700">
            <Icon name="mdi:email" class="text-orange-500 mr-2" />
            knapen@ksaizegem.be
          </p>
        </div>

        <!-- Jonghernieuwers -->
        <div>
          <NuxtImg
            src="/jonghernieuwers.png"
            alt="Jonghernieuwers"
            class="w-40 mx-auto mb-4"
          />
          <h3 class="text-xl font-semibold">Jonghernieuwers</h3>
          <p class="text-gray-600 mb-2">14-16 jaar (3e en 4e secundair)</p>
          <p class="flex items-center justify-center text-gray-700">
            <Icon name="mdi:email" class="text-orange-500 mr-2" />
            jonghernieuwers@ksaizegem.be
          </p>
        </div>

        <!-- Hernieuwers -->
        <div>
          <NuxtImg
            src="/hernieuwers.png"
            alt="Hernieuwers"
            class="w-40 mx-auto mb-4"
          />
          <h3 class="text-xl font-semibold">Hernieuwers</h3>
          <p class="text-gray-600 mb-2">16-17 jaar (5e en 6e secundair)</p>
          <p class="flex items-center justify-center text-gray-700">
            <Icon name="mdi:email" class="text-orange-500 mr-2" />
            hernieuwers@ksaizegem.be
          </p>
        </div>

        <!-- Bond -->
        <div>
          <NuxtImg src="/ksa-icoon.png" alt="Bond" class="w-40 mx-auto mb-4" />
          <h3 class="text-xl font-semibold">Bond</h3>
          <p class="text-gray-600 mb-2">Oud</p>
          <p class="flex items-center justify-center text-gray-700">
            <Icon name="mdi:email" class="text-orange-500 mr-2" />
            bond@ksaizegem.be
          </p>
        </div>

        <!-- VZW -->
        <div>
          <NuxtImg src="/ksa-icoon.png" alt="VZW" class="w-40 mx-auto mb-4" />
          <h3 class="text-xl font-semibold">VZW</h3>
          <p class="text-gray-600 mb-2">Oud</p>
          <p class="flex items-center justify-center text-gray-700">
            <Icon name="mdi:email" class="text-orange-500 mr-2" />
            vzw@ksaizegem.be
          </p>
        </div>
      </div>
    </section>

    <FooterComponent />
  </div>
</template>
