<template>
  <q-card bordered class="service-card">
    <q-img :src="service.imgSrc" :alt="service.title" class="q-mb-sm" />
    <q-card-section>
      <p class="text-h6 text-weight-bold">{{ service.title }}</p>
      <p class="text-subtitle2">{{ service.description }}</p>
    </q-card-section>
  </q-card>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  service: {
    type: Object,
    required: true,
    default: () => ({
      title: "",
      description: "",
      imgSrc: "",
    }),
  },
});
</script>

<style scoped>
.service-card {
  max-width: 300px;
  margin: 1rem;
}
</style>
