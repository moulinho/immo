<template>
  <div class="bg-black q-py-lg" id="project">
    <div class="row justify-center q-my-md q-px-xl">
      <q-separator spaced inset size=".5rem" color="amber-8" class="col-1" />
    </div>
    <p class="text-h5 text-weight-bolder text-amber-8 text-center">
      Réalisations
    </p>
    <q-carousel
      v-model="slideRealisation"
      transition-prev="slide-right"
      transition-next="slide-left"
      swipeable
      animated
      infinite
      control-color="amber-8"
      navigation
      padding
      arrows
      :autoplay="2500"
      height="350px"
      class="bg-grey-9 shadow-2 rounded-borders"
    >
      <q-carousel-slide
        v-for="(group, index) in realisationGroups"
        :key="index"
        :name="index + 1"
        class="column no-wrap"
      >
        <div
          class="row fit justify-center items-center q-gutter-xs q-col-gutter no-wrap"
        >
          <q-img
            v-for="item in group"
            :key="item.src"
            :alt="item.caption"
            :src="item.src"
            :position="item.position ?? '50% 50%'"
            class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
          >
            <div class="absolute-bottom text-center">{{ item.caption }}</div>
          </q-img>
        </div>
      </q-carousel-slide>
    </q-carousel>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { realisations } from "src/data/siteData.js";

const slideRealisation = ref(1);

const realisationGroups = [];
for (let i = 0; i < realisations.length; i += 3) {
  realisationGroups.push(realisations.slice(i, i + 3));
}
</script>
