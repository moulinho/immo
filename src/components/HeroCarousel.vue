<template>
  <q-carousel
    v-model="slide"
    transition-prev="jump-right"
    transition-next="jump-left"
    swipeable
    animated
    infinite
    control-color="white"
    prev-icon="arrow_left"
    next-icon="arrow_right"
    navigation-icon="radio_button_unchecked"
    navigation
    padding
    arrows
    :autoplay="2500"
    height="500px"
    class="bg-transparent"
  >
    <q-carousel-slide
      v-for="hero in heroSlides"
      :key="hero.name"
      :name="hero.name"
      :img-src="hero.img"
      class="column no-wrap justify-center"
    >
      <div class="row">
        <div :class="hero.paddingClass" style="backdrop-filter: blur(1px)">
          <p
            :class="
              $q.screen.lt.sm
                ? 'text-h4 text-weight-bold'
                : 'text-h3 text-weight-bold'
            "
          >
            {{ hero.title }}
          </p>
          <q-btn color="amber-8" rounded unelevated class="q-px-lg" no-caps>
            <a href="#devis" class="text-white">Obtenir un devis gratuit</a>
          </q-btn>
        </div>
      </div>
    </q-carousel-slide>
  </q-carousel>
</template>

<script setup>
import { ref } from "vue";
import { heroSlides } from "src/data/siteData.js";

const slide = ref(heroSlides[0].name);
</script>
