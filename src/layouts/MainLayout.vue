<template>
  <q-layout view="lHh Lpr lff">
    <q-header elevated class="bg-white">
      <q-banner class="bg-negative text-center">
        Nous tenons à vous informer que votre contrat d'hébergement arrive à
        expiration le 22/04/2024 à 23:59:59. Nous apprécions sincèrement votre
        confiance en notre service jusqu'à présent. Afin de garantir la
        continuité de votre présence en ligne, nous vous encourageons à
        renouveler votre abonnement dès que possible. Le non-renouvellement de
        votre hébergement entraînera la désactivation de votre site web
      </q-banner>
      <q-toolbar class="q-py-sm q-px-lg">
        <q-toolbar-title
          :class="$q.screen.lt.sm ? 'col row items-end' : 'col-4 row items-end'"
        >
          <q-img
            src="~assets/Logo.png"
            spinner-color="amber"
            spinner-size="82px"
            width="70px"
          />
        </q-toolbar-title>
        <div class="col row justify-end">
          <q-btn
            flat
            dense
            round
            color="black"
            icon="menu"
            aria-label="Menu"
            @click="toggleLeftDrawer"
            v-if="$q.screen.lt.sm"
          />
          <q-tabs v-model="tab" indicator-color="amber" align="justify" v-else>
            <q-tab name="home" no-caps class="q-ml-md" href="#home">
              <a href="#home" class="text-black text-weight-bold"> Acceuil</a>
            </q-tab>
            <q-tab name="about" no-caps class="q-ml-md">
              <a href="#about" class="text-black text-weight-bold">
                À propos
              </a>
            </q-tab>
            <q-tab name="services" no-caps class="q-ml-md" href="#services">
              <a href="#services" class="text-black text-weight-bold">
                Services
              </a>
            </q-tab>
            <q-tab name="project" no-caps class="q-ml-md" href="#project">
              <a href="#project" class="text-black text-weight-bold">
                Réalisations
              </a>
            </q-tab>
            <!-- <q-tab name="blog" label="Blog" no-caps /> -->
            <q-tab name="devis" href="#devis" no-caps class="q-ml-md">
              <a href="#devis" class="text-black text-weight-bold"> Devis </a>
            </q-tab>
            <q-btn
              color="amber-8"
              rounded
              unelevated
              class="q-px-lg q-ml-xl"
              no-caps
            >
              <a
                href="mailto:societecariere@gmail.com"
                class="text-white"
                style="text-decoration: none"
              >
                Contacts
              </a>
            </q-btn>
          </q-tabs>
        </div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" bordered class="q-pa-lg bg-amber-1">
      <div class="text-black column items-center text-weight-bold q-gutter-lg">
        <q-item clickable tag="a" href="#home">
          <q-item-section>
            <q-item-label>Acceuil</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" href="#about">
          <q-item-section>
            <q-item-label>À propos</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" href="#services">
          <q-item-section>
            <q-item-label>Services</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" href="#project">
          <q-item-section>
            <q-item-label>Réalisations</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" href="#devis">
          <q-item-section>
            <q-item-label>Devis</q-item-label>
          </q-item-section>
        </q-item>

        <div class="row">
          <q-btn color="amber-8" rounded unelevated class="col" no-caps>
            <a
              href="mailto:societecariere@gmail.com"
              class="text-white"
              style="text-decoration: none"
            >
              Contacts
            </a>
          </q-btn>
        </div>
      </div>
    </q-drawer>

    <q-footer class="bg-black q-pa-md">
      <div class="row justify-center q-my-md q-px-xl">
        <q-separator spaced inset size=".5rem" color="amber-8" class="col-1" />
      </div>
      <div class="row justify-around q-py-md">
        <div class="col-md-7 col-sm-7 col-xs-12">
          <p class="text-body1 text-weight-bolder">
            CARIERE- SARL au capital de 1 000 000 FCFA
          </p>
          <div class="text-weight-medium">
            Siège sociale : Abidjan, Yopougon, Millionnaire vers la CGRAE - 23
            bp 240 Abidjan 23 <br />RCCM : CI-ABJ-03-2023-b13-04490 <br />
            IDU : CI -2023-0049483 I <br />Tèl : (+225) 01 01 73 85 00 <br />
            Email :
            <!-- <q-btn
              color=""
              label="ouattraamadou@gmail.com"
              to="mailto:jim@example.com"
            /> -->
            <a
              href="mailto:societecariere@gmail.com"
              class="text-white"
              style="text-decoration: none"
            >
              societecariere@gmail.com
            </a>
            <div class="">
              <q-btn
                icon="img:icons/facebook.svg"
                size="lg"
                class="q-pl-none"
              />
              <q-btn
                icon="img:icons/whatsapp.svg"
                size="lg"
                class="q-pl-none"
              />
              <q-btn
                icon="img:icons/linkedin.svg"
                size="lg"
                class="q-pl-none"
              />
            </div>
          </div>
        </div>
        <div class="col-md-3 col-sm-3 col-xs-12">
          <p class="text-h5 text-weight-bolder">Liens utiles</p>
          <div class="text-body1">
            Partenaires & Aﬃliation <br />
            Conditions générales d'utilisation
          </div>
        </div>
      </div>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";
import EssentialLink from "components/EssentialLink.vue";

defineOptions({
  name: "MainLayout",
});

const linksList = [
  {
    title: "Docs",
    caption: "quasar.dev",
    icon: "school",
    link: "https://quasar.dev",
  },
  {
    title: "Github",
    caption: "github.com/quasarframework",
    icon: "code",
    link: "https://github.com/quasarframework",
  },
  {
    title: "Discord Chat Channel",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: "https://chat.quasar.dev",
  },
  {
    title: "Forum",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev",
  },
  {
    title: "Twitter",
    caption: "@quasarframework",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev",
  },
  {
    title: "Facebook",
    caption: "@QuasarFramework",
    icon: "public",
    link: "https://facebook.quasar.dev",
  },
  {
    title: "Quasar Awesome",
    caption: "Community Quasar projects",
    icon: "favorite",
    link: "https://awesome.quasar.dev",
  },
];

const leftDrawerOpen = ref(false);

const tab = ref("home");

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
