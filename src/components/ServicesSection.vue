<template>
  <div class="bg-lime-1 q-py-lg" id="services">
    <div class="row justify-center q-my-md q-px-xl">
      <q-separator spaced inset size=".5rem" color="black" class="col-1" />
    </div>
    <p class="text-h5 text-weight-bolder text-center">Services</p>
    <div class="row justify-center q-gutter-md q-px-xl">
      <ServiceCard v-for="service in services" :key="service.title" :service="service" />
    </div>
  </div>
</template>

<script setup>
import ServiceCard from "src/components/ServiceCard.vue";
import { services } from "src/data/siteData.js";
</script>
