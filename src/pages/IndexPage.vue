<template>
  <q-page class="" id="home">
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
      <!-- autoplay="2500" -->
      <q-carousel-slide
        name="style"
        img-src="../assets/representation-construction-industry.webp"
        class="column no-wrap justify-center"
      >
        <div class="row">
          <div class="" style="backdrop-filter: blur(1px)">
            <p
              :class="
                $q.screen.lt.sm
                  ? 'text-h4 text-weight-bold'
                  : 'text-h3 text-weight-bold'
              "
            >
              CONSTRUCTION AMENAGEMENT <br />RESEAUX INGENIERIE
            </p>

            <q-btn
              color="amber-8"
              rounded
              unelevated
              label="Obtenir un devis gratuit"
              class="q-px-lg"
              no-caps
            />
          </div>
        </div>
      </q-carousel-slide>

      <q-carousel-slide
        name="tv"
        img-src="../assets/img6.jpg"
        class="column no-wrap justify-center"
      >
        <div class="row">
          <div class="q-ma-xl" style="backdrop-filter: blur(1px)">
            <p
              :class="
                $q.screen.lt.sm
                  ? 'text-h4 text-weight-bold'
                  : 'text-h3 text-weight-bold'
              "
            >
              EQUIPEMENT ROUTES ET <br />
              ELECTIFICATION
            </p>

            <q-btn
              color="amber-8"
              rounded
              unelevated
              label="Obtenir un devis gratuit"
              class="q-px-lg"
              no-caps
            />
          </div>
        </div>
      </q-carousel-slide>
    </q-carousel>
    <div class="row justify-center q-my-md" id="about">
      <q-separator spaced inset size=".6rem" color="amber-8" class="col-1" />
    </div>
    <P class="text-h5 text-weight-bolder text-center"> À propos </P>

    <div class="q-pa-md">
      <p class="text-center text-h4 text-weight-bold">
        Leader du BTP en Afrique, nous sommes l’entreprise de <br />
        construction de référence.
      </p>
      <p class="text-h5 text-body1 text-justify text-weight-regular q-pa-xl">
        Lorem Ipsum is simply dummy text of the printing and typesetting
        industry. Lorem Ipsum has been the industry's standard dummy text ever
        since the 1500s, when an unknown printer took a galley of type and
        scrambled it to make a type specimen book. It has survived not only ﬁve
        centuries, but also the leap into electronic typesetting, remaining
        essentially unchanged. It was popularised in the 1960s with the release
        of Letraset sheets containing Lorem Ipsum passages, and more recently
        with desktop publishing software like Aldus PageMaker including versions
        of Lorem Ipsum.
      </p>
    </div>
    <div class="bg-lime-1 q-py-lg" id="services">
      <div class="row justify-center q-my-md">
        <q-separator spaced inset size=".6rem" color="black" class="col-1" />
      </div>
      <P class="text-h5 text-weight-bolder text-center"> Services </P>
      <div class="row justify-center q-gutter-md q-px-xl">
        <q-card
          class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-py-lg q-px-md"
        >
          <q-avatar size="8rem">
            <q-img
              alt="img-btp"
              src="~assets/bati.jpg"
              style="border-radius: 50%"
              width="100%"
              height="100%"
            />
          </q-avatar>

          <q-card-section>
            <div class="text-h6">Bâtiment</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            with desktop publishing software like Aldus PageMaker including
            versions of Lorem Ipsum.
          </q-card-section>
        </q-card>
        <q-card
          class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-py-lg q-px-md"
        >
          <q-avatar size="8rem">
            <q-img
              alt="img-btp"
              src="~assets/img.jpeg"
              style="border-radius: 50%"
              width="100%"
              height="100%"
            />
          </q-avatar>

          <q-card-section>
            <div class="text-h6">Travaux Publics</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            with desktop publishing software like Aldus PageMaker including
            versions of Lorem Ipsum.
          </q-card-section>
        </q-card>
        <q-card
          class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-py-lg q-px-md"
        >
          <q-avatar size="8rem">
            <q-img
              alt="img-btp"
              src="~assets/placement.jpg"
              style="border-radius: 50%"
              width="100%"
              height="100%"
            />
          </q-avatar>
          <!-- <q-avatar
            size="100px"
            font-size="52px"
            color="teal"
            text-color="white"
            icon="img:icons/loti.jpg"
          /> -->

          <q-card-section>
            <div class="text-h6">Placement de Personnel BTP</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            with desktop publishing software like Aldus PageMaker including
            versions of Lorem Ipsum.
          </q-card-section>
        </q-card>
        <q-card
          class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-py-lg q-px-md"
        >
          <q-avatar size="8rem">
            <q-img
              alt="img-btp"
              src="~assets/engin.jpg"
              style="border-radius: 50%"
              width="100%"
              height="100%"
            />
          </q-avatar>
          <!-- <q-avatar
            size="100px"
            font-size="52px"
            color="teal"
            text-color="white"
            icon="img:icons/loti.jpg"
          /> -->

          <q-card-section>
            <div class="text-h6">Location Engins de Chantier</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            with desktop publishing software like Aldus PageMaker including
            versions of Lorem Ipsum.
          </q-card-section>
        </q-card>
        <q-card
          class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-py-lg q-px-md"
        >
          <q-avatar size="8rem">
            <q-img
              alt="img-btp"
              src="~assets/loti.jpg"
              style="border-radius: 50%"
              width="100%"
              height="100%"
            />
          </q-avatar>

          <q-card-section>
            <div class="text-h6">Lotissements</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            with desktop publishing software like Aldus PageMaker including
            versions of Lorem Ipsum.
          </q-card-section>
        </q-card>
        <q-card
          class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-py-lg q-px-md"
        >
          <q-avatar size="8rem">
            <q-img
              alt="img-btp"
              src="~assets/electrification.jpg"
              style="border-radius: 50%"
              width="100%"
              height="100%"
            />
          </q-avatar>

          <q-card-section>
            <div class="text-h6">Electrification</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            with desktop publishing software like Aldus PageMaker including
            versions of Lorem Ipsum.
          </q-card-section>
        </q-card>

        <q-card
          class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-py-lg q-px-md"
        >
          <q-avatar size="8rem">
            <q-img
              alt="img-btp"
              src="~assets/Matériel-de-chantier.jpg"
              style="border-radius: 50%"
              width="100%"
              height="100%"
            />
          </q-avatar>
          <!-- <q-avatar
            size="100px"
            font-size="52px"
            color="teal"
            text-color="white"
            icon="img:icons/loti.jpg"
          /> -->

          <q-card-section>
            <div class="text-h6">vente de matériel et matériaux du btp</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            with desktop publishing software like Aldus PageMaker including
            versions of Lorem Ipsum.
          </q-card-section>
        </q-card>
      </div>
    </div>
    <div class="bg-black q-py-lg" id="project">
      <div class="row justify-center q-my-md">
        <q-separator spaced inset size=".6rem" color="amber-8" class="col-1" />
      </div>
      <P class="text-h5 text-weight-bolder text-amber-8 text-center">
        Réalisations
      </P>
      <q-carousel
        v-model="slideRealsation"
        transition-prev="slide-right"
        transition-next="slide-left"
        swipeable
        animated
        control-color="amber-8"
        navigation
        padding
        arrows
        :autoplay="2500"
        height="350px"
        class="bg-grey-9 shadow-2 rounded-borders"
      >
        <q-carousel-slide :name="1" class="column no-wrap">
          <div
            class="row fit justify-center items-center q-gutter-xs q-col-gutter no-wrap"
          >
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/img4.jpeg"
            >
              <div class="absolute-bottom text-center">
                <!-- Ouverture de voies à azaguie -->
                Immeuble r+2 à Yopougon
              </div>
            </q-img>
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 11.47.47.jpeg"
            >
              <div class="absolute-bottom text-center">
                Extension réseau Yopougon
              </div>
            </q-img>
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 11.50.20.jpeg"
            >
              <div class="absolute-bottom text-center">
                Extension réseau à Akeikoi et à Alepe
              </div>
            </q-img>
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="2" class="column no-wrap">
          <div
            class="row fit justify-center items-center q-gutter-xs q-col-gutter no-wrap"
          >
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 11.54.19.jpeg"
            >
              <div class="absolute-bottom text-center">
                Ouverture de voies pour pose de poteaux BT
              </div>
            </q-img>
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 11.58.33.jpeg"
              position="50% 40%"
            >
              <div class="absolute-bottom text-center">
                Ouverture de voies à azaguie
              </div>
            </q-img>
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/engin.jpg"
              fit=""
            >
              <div class="absolute-bottom text-center">
                Ouverture de voies à azaguie
              </div>
            </q-img>
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="3" class="column no-wrap">
          <div
            class="row fit justify-center items-center q-gutter-xs q-col-gutter no-wrap"
          >
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 12.03.20.jpeg"
              position="50% 30%"
            >
              <div class="absolute-bottom text-center">
                Terrassement à bassam
              </div>
            </q-img>
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 12.15.39.jpeg"
              position="50% 20%"
            >
              <div class="absolute-bottom text-center">
                Terrassement à azaguie
              </div>
            </q-img>
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/img5.jpeg"
              position="50% 10%"
            >
              <div class="absolute-bottom text-center">
                Terrassement à malbert
              </div>
            </q-img>
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="4" class="column no-wrap">
          <div
            class="row fit justify-center items-center q-gutter-xs q-col-gutter no-wrap"
          >
            <q-img
              alt="img-btp"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/img.jpeg"
            >
              <div class="absolute-bottom text-center">
                Construction de villas à songon
              </div>
            </q-img>
            <q-img
              alt="img-btp"
              class="rounded-borders col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 12.29.29.jpeg"
            >
              <div class="absolute-bottom text-center">
                Construction de villas à songon
              </div>
            </q-img>
            <q-img
              alt="img-btp"
              class="rounded-borders col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 12.32.19.jpeg"
            >
              <div class="absolute-bottom text-center">Travaux de finition</div>
            </q-img>
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
    <!-- <div class="">
      <div class="row justify-center q-my-md">
        <q-separator spaced inset size=".6rem" color="black" class="col-1" />
      </div>
      <P class="text-h5 text-weight-bolder text-center"> Services </P>
      <div class="row justify-evenly items-center q-pa-md">
        <div class="col-md-5 col-sm-5 col-xs-12">
          <div class="q-ma-xl" style="backdrop-filter: blur(1px)">
            <p class="text-h5 text-weight-bold">
              CONSTRUCTION AMENAGEMENT RESEAUX INGENIERIE EQUIPEMENT ROUTES ET
              ELECTIFICATION
            </p>
            <p class="text-body1">
              Lorem Ipsum is simply dummy text of the printing and <br />
              typesetting industry. Lorem Ipsum has been the
            </p>
            <q-btn
              color="amber-8"
              rounded
              unelevated
              label="Obtenir un devis gratuit"
              class="q-px-lg"
              no-caps
              @click="onClick"
            />
          </div>
        </div>
        <div class="col-md-3 col-sm-4 col-xs-12">
          <q-img
            alt="img-btp"
            src="~assets/2150440920.jpg"
            spinner-color="primary"
            width="100%"
            height="35rem"
            spinner-size="82px"
          />
        </div>
      </div>
    </div> -->

    <!-- <div class="row justify-center q-my-md">
      <q-separator spaced inset size=".6rem" color="amber-8" class="col-1" />
    </div>
    <P class="text-h5 text-weight-bolder text-center"> Devis </P>

    <div class="q-pa-md row">
      <div class="col">
        <q-input v-model="text" type="text" label="Label" />
      </div>
      <div class="col"></div>
    </div> -->
  </q-page>
</template>

<script setup>
import { ref } from "vue";

defineOptions({
  name: "IndexPage",
});

const slide = ref("style");
const slideRealsation = ref(1);
</script>
