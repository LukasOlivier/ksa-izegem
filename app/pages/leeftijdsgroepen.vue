<template>
  <div>
    <HeaderComponent />

    <!-- Hero Section -->
    <section class="container mx-auto px-6 my-40 max-w-5xl text-center">
      <h1 class="md:text-5xl text-4xl font-bold mb-20">Leeftijdsgroepen</h1>

      <!-- Leeftijdsgroepen -->
      <div class="space-y-40">
        <div
          v-for="(group, idx) in groups"
          :key="group.name"
          :class="[
            'relative flex flex-col items-center justify-between gap-10',
            idx % 2 === 1 ? 'md:flex-row-reverse' : 'md:flex-row',
          ]"
        >
          <NuxtImg
            :src="group.img"
            :alt="group.name"
            class="object-contain md:max-w-md max-w-sm"
          />
          <div class="text-left max-w-2xl">
            <h2 class="text-3xl font-bold text-orange-600 mb-2">
              {{ group.name }}
            </h2>
            <p class="text-ksa_blue mb-3 font-semibold">
              Leeftijd: {{ group.age }}
            </p>
            <p class="text-gray-700 leading-relaxed">
              {{ group.description }}
            </p>
            <!-- Download button with icon -->
            <a
              :href="group.schedule"
              download
              class="mt-4 px-3 py-2 text-orange-500 rounded border-2 border-orange-500 transition hover:bg-orange-600 hover:text-white font-medium inline-flex items-center gap-2"
            >
              <Icon name="mdi:download" size="22" />
              Programma boekje
            </a>
          </div>
        </div>
      </div>
    </section>

    <FooterComponent />
  </div>
</template>

<script setup>
  const groups = [
    {
      name: 'Kabouters',
      img: '/monster-kabouters.png',
      age: '6-8 jaar (1e en 2e leerjaar)',
      description:
        'De jongste leden van onze beweging noemen we de Kabouters. KSA betekent voor hen spelen, spelen en nog eens spelen. Ze kunnen zich op elke activiteit volledig uitleven. Hun kinderlijke fantasie zorgt ervoor dat ze zich uren kunnen amuseren met water, zand, verf en ander, voor veel probleem, of ze toveren met eenvoudig knutselmateriaal de mooiste dingen.',
      schedule:
        'https://drive.google.com/uc?export=download&id=1uuV4zjCcTsGL5IW1ZgMGuxLUoPG6xXfx',
    },
    {
      name: 'Piepjongknapen',
      img: '/monster-piepjongknapen.png',
      age: '8-10 jaar (3e en 4e leerjaar)',
      description:
        'De Piepjongknapen zitten halfweg hun carrière op de lagere school en zijn niet langer de jongste leden van KSA. Het is een enthousiaste bende die geregeld al echt samen kan spelen. De spelletjes worden al wat complexer. Lang stilzitten is niet aan hen besteed, in onze jeugdbeweging kunnen ze bewegen en van alles uitproberen wat thuis niet kan.',
      schedule:
        'https://drive.google.com/uc?export=download&id=1uuV4zjCcTsGL5IW1ZgMGuxLUoPG6xXfx',
    },
    {
      name: 'Jongknapen',
      img: '/monster-jongknapen.png',
      age: '10-12 jaar (5e en 6e leerjaar)',
      description:
        'De Jongknapen vinden in KSA vooral actie en spanning. Ze mogen zelf al eens het initiatief nemen om de activiteiten wat op te vullen, al houdt de leiding steeds een oogje in het zeil. Ze zijn de waaghalzen van KSA die graag in competitie treden met elkaar. In de jeugdbeweging mogen ze echt bij de groep horen en nieuwe vrienden leren kennen.',
      schedule:
        'https://drive.google.com/uc?export=download&id=1uuV4zjCcTsGL5IW1ZgMGuxLUoPG6xXfx',
    },
    {
      name: 'Knapen',
      img: '/monster-knapen.png',
      age: '12-14 jaar (1e en 2e secundair)',
      description:
        'De leden van 12 tot 14 jaar heten in KSA de Knapen. Ze zijn stilaan "groot" geworden en mogen de echte wereld gaan verkennen. Ze gebruiken de vrijheid die ze genieten als pubers om op avontuur te trekken. Ook in KSA kunnen ze met vanalles gaan experimenteren. Die groep avonturiers is al redelijk zelfstandig geworden in al wat ze doen. Aangezien Knapen, Jimmers en Knimmers volop zichzelf aan het ontdekken zijn, leidt dat geregeld eens tot kleine crisissen waar de leiding als moderator nodig is. De activiteiten worden al heel wat avontuurlijker en de vriendengroep heel wat hechter.',
      schedule:
        'https://drive.google.com/uc?export=download&id=1uuV4zjCcTsGL5IW1ZgMGuxLUoPG6xXfx',
    },
    {
      name: 'Jonghernieuwers',
      img: '/monster-jonghernieuwers.png',
      age: '14-16 jaar (3e en 4e secundair)',
      description:
        'KSA wordt voor de Jonghernieuwers een ontmoetingsplaats met vrienden. Ze willen soms eens stilzitten om wat gezellig te babbelen, maar trekken er even graag samen op uit om de meest uiteenlopende stunts te beleven. De leiding zet activiteiten op die een uitdaging vormen voor de leden en hen uitnodigen om samen te werken om hun doel te bereiken. Er wordt al heel wat verantwoordelijkheid doorgespeeld naar de leden en de groep mag geregeld zelf één en ander organiseren. In KSA mogen ze zichzelf zijn, los van de doordeweekse verplichtingen en verwachtingen.',
      schedule:
        'https://drive.google.com/uc?export=download&id=1uuV4zjCcTsGL5IW1ZgMGuxLUoPG6xXfx',
    },
    {
      name: 'Hernieuwers',
      img: '/monster-hernieuwers.png',
      age: '16-17 jaar (5e en 6e secundair)',
      description:
        'Eens je 16 jaar geworden bent in KSA maken leden de overstap van lid naar leiding in opleiding. Voor hen worden wat activiteiten georganiseerd, maar ze leren ook de kneepjes kennen van het leiding-zijn. Ze zijn actief bezig een eigen identiteit op te bouwen en daarin kan KSA een belangrijke rol spelen. Ze nemen een zeker engagement op binnen de groep en hebben inspraak in de richting die het uit moet. Ze maken plannen en keuzes voor de toekomst en denken na over de maatschappij en hoe die er zou moeten uitzien. Als jongeren kiezen ze ervoor zelf de handen uit de mouwen te steken en een steen(tje) bij te dragen. Daarnaast draait het natuurlijk vaak om gewoon in groep plezier maken en je eens uitleven, zonder je al te veel te moeten aantrekken van de eisen van de "volwassen wereld" (het blijft nog altijd jeugdbeweging).',
      schedule:
        'https://drive.google.com/uc?export=download&id=1uuV4zjCcTsGL5IW1ZgMGuxLUoPG6xXfx',
    },
  ];
</script>
