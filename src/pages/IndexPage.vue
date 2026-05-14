<template>
  <q-page id="home">
    <HeroCarousel />

    <!-- À propos -->
    <div class="row justify-center q-my-md q-px-xl" id="about">
      <q-separator spaced inset size=".5rem" color="amber-8" class="col-1" />
    </div>
    <p class="text-h5 text-weight-bolder text-center">À propos</p>
    <div class="q-pa-md">
      <p class="text-center text-h4 text-weight-bold">
        Leader du BTP en Afrique, nous sommes l'entreprise de <br />
        construction de référence.
      </p>
      <p class="text-h5 text-h6 text-center text-weight-regular q-pa-xl">
        Cariere est une société créée par des professionnels du secteur du BTP
        venant de différentes entreprises de la place les différents
        travailleurs se connaissaient depuis 2006 déjà et faisaient chemin
        ensemble.
      </p>
    </div>

    <ServicesSection />
    <RealisationsSection />
    <DevisForm />
  </q-page>
</template>

<script setup>
import HeroCarousel from "src/components/HeroCarousel.vue";
import ServicesSection from "src/components/ServicesSection.vue";
import RealisationsSection from "src/components/RealisationsSection.vue";
import DevisForm from "src/components/DevisForm.vue";

defineOptions({ name: "IndexPage" });
</script>
