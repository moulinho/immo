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
        img-src="~assets/representation-construction-industry.webp"
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

            <q-btn color="amber-8" rounded unelevated class="q-px-lg" no-caps>
              <a href="#devis" class="text-white"> Obtenir un devis gratuit</a>
            </q-btn>
          </div>
        </div>
      </q-carousel-slide>

      <q-carousel-slide
        name="tv"
        img-src="~assets/img6.jpg"
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

            <q-btn color="amber-8" rounded unelevated class="q-px-lg" no-caps>
              <a href="#devis" class="text-white"> Obtenir un devis gratuit </a>
            </q-btn>
          </div>
        </div>
      </q-carousel-slide>
    </q-carousel>
    <div class="row justify-center q-my-md q-px-xl" id="about">
      <q-separator spaced inset size=".5rem" color="amber-8" class="col-1" />
    </div>
    <P class="text-h5 text-weight-bolder text-center"> À propos </P>

    <div class="q-pa-md">
      <p class="text-center text-h4 text-weight-bold">
        Leader du BTP en Afrique, nous sommes l’entreprise de <br />
        construction de référence.
      </p>
      <p class="text-h5 text-h6 text-center text-weight-regular q-pa-xl">
        Cariere est une société créée par des professionnels du secteur du BTP
        venant de différentes entreprises de la place les différents
        travailleurs se connaissaient depuis 2006 déjà et faisaient chemin
        ensemble.
      </p>
    </div>
    <div class="bg-lime-1 q-py-lg" id="services">
      <div class="row justify-center q-my-md q-px-xl">
        <q-separator spaced inset size=".5rem" color="black" class="col-1" />
      </div>
      <P class="text-h5 text-weight-bolder text-center"> Services </P>
      <div class="row justify-center q-gutter-md q-px-xl">
        <!-- <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
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
            Construction, Amenagement et réseaux
          </q-card-section>
        </q-card> -->
        <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
          <q-avatar size="8rem">
            <q-img
              alt="travaux publics"
              src="~assets/img.jpeg"
              style="border-radius: 50%"
              width="100%"
              height="100%"
            />
          </q-avatar>

          <q-card-section>
            <div class="text-h6">Travaux publics</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            Assainissement et gestion des eaux, Infrastructure routière, Génie
            civil et construction, Aménagement urbain et paysager , Sécurité
            publique
          </q-card-section>
        </q-card>
        <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
          <q-avatar size="8rem">
            <q-img
              alt="img-btp"
              src="~assets/placement.webp"
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
            <div class="text-h6">Formation BTP</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            Formation initiale ,Formation spécialisée, L'études de projet,
            Apprentissage.
          </q-card-section>
        </q-card>
        <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
          <q-avatar size="8rem">
            <q-img
              alt="img-btp"
              src="~assets/engin.webp"
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
            <div class="text-h6">Location engins de chantier</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            <!-- Le reprofilage de voies -->
            Pelleteuses, Bulldozers, Compacteurs, Grues, Camions-bennes,
            Camions-grues, Chariots élévateurs
          </q-card-section>
        </q-card>
        <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
          <q-avatar size="8rem">
            <q-img
              alt="Lotissements"
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
            Construction, Amenagement et réseaux.
          </q-card-section>
        </q-card>
        <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
          <q-avatar size="8rem">
            <q-img
              alt="Electrification"
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
            L'électrification rural et pose de poste la fabrication de poteaux
            électriques.
          </q-card-section>
        </q-card>

        <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
          <q-avatar size="8rem">
            <q-img
              alt="matériaux"
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
            <div class="text-h6">Matériel et matériaux du btp</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            Vente et location des matériels et matériaux du btp
          </q-card-section>
        </q-card>

        <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
          <q-avatar size="8rem">
            <q-img
              alt="Reprofilage"
              src="~assets/img5.jpeg"
              style="border-radius: 50%"
              position="40% 10%"
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
            <div class="text-h6">Reprofilage de voies</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            Évaluation de l'état des voies, Planification des travaux,
            Préparation du chantier, Contrôle qualité, Nettoyage et remise en
            service
          </q-card-section>
        </q-card>

        <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
          <q-avatar size="8rem">
            <q-img
              alt="terrassements"
              src="~assets/4806.webp"
              style="border-radius: 50%"
              position="40% 10%"
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
            <div class="text-h6">Les terrassements</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            Étude géotechnique, Défrichage et démolition, Déblaiement,
            Remblayage, Modelage du terrain, Contrôle qualité et finition
          </q-card-section>
        </q-card>
      </div>
    </div>
    <div class="bg-black q-py-lg" id="project">
      <div class="row justify-center q-my-md q-px-xl">
        <q-separator spaced inset size=".5rem" color="amber-8" class="col-1" />
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
        infinite
        :autoplay="2500"
        height="350px"
        class="bg-grey-9 shadow-2 rounded-borders"
      >
        <q-carousel-slide :name="1" class="column no-wrap">
          <div
            class="row fit justify-center items-center q-gutter-xs q-col-gutter no-wrap"
          >
            <q-img
              alt="Immeuble"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/img4.jpeg"
            >
              <div class="absolute-bottom text-center">
                <!-- Ouverture de voies à azaguie -->
                Immeuble r+2 à Yopougon
              </div>
            </q-img>
            <q-img
              alt="Extension réseau"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 11.47.47.jpeg"
              position="50% 40%"
            >
              <div class="absolute-bottom text-center">
                Extension réseau Yopougon
              </div>
            </q-img>
            <q-img
              alt="Extension réseau Akeikoi"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 11.50.20.jpeg"
              position="50% 40%"
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
              alt="Ouverture de voies"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 11.54.19.jpeg"
            >
              <div class="absolute-bottom text-center">
                Ouverture de voies pour pose de poteaux BT
              </div>
            </q-img>
            <q-img
              alt="azaguie"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 11.58.33.jpeg"
              position="50% 40%"
            >
              <div class="absolute-bottom text-center">
                Ouverture de voies à azaguie
              </div>
            </q-img>
            <q-img
              alt="engin"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/engin.webp"
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
              alt="Terrassement à bassam"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 12.03.20.jpeg"
              position="50% 30%"
            >
              <div class="absolute-bottom text-center">
                Terrassement à bassam
              </div>
            </q-img>
            <q-img
              alt="Terrassement à azaguie"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 12.15.39.jpeg"
              position="50% 20%"
            >
              <div class="absolute-bottom text-center">
                Terrassement à azaguie
              </div>
            </q-img>
            <q-img
              alt="Terrassement à malbert"
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
              alt="Construction"
              class="rounded-borders col-md-3 col-sm-3 col-xs-6 full-height"
              src="~assets/img.jpeg"
            >
              <div class="absolute-bottom text-center">
                Construction de villas à songon
              </div>
            </q-img>
            <q-img
              alt="Construction"
              class="rounded-borders col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 12.29.29.jpeg"
            >
              <div class="absolute-bottom text-center">
                Construction de villas à songon
              </div>
            </q-img>
            <q-img
              alt="Travaux de finition"
              class="rounded-borders col-sm-3 col-xs-6 full-height"
              src="~assets/WhatsApp Image 2024-04-13 at 12.32.19.jpeg"
            >
              <div class="absolute-bottom text-center">Travaux de finition</div>
            </q-img>
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
    <div class="bg-lime-1 q-py-lg" id="devis">
      <div class="row justify-center q-my-md q-px-xl">
        <q-separator spaced inset size=".5rem" color="black" class="col-1" />
      </div>
      <p class="text-h5 text-black text-center q-px-lg">
        Vous avez un projet immobilier à Abidjan, en Côte d’Ivoire ou dans la
        sous-région ? Nous avons l’expertise pour le réaliser au-delà de vos
        espérances ! Nombreux sont ceux qui nous sollicitent chaque jour et qui
        repartent satisfaits.
      </p>
      <p class="text-h5 text-black text-center q-px-lg">
        Soumettez-nous simplement votre demande pour obtenir un devis estimatif
        détaillé de votre projet. Nous sommes déjà ravis de commencer avec vous
        une nouvelle collaboration à succès !
      </p>
      <P class="text-h4 text-weight-bolder text-black text-center q-pa-lg">
        FORMULAIRE DE DEMANDE DE DEVIS
      </P>
      <div class="row justify-center q-my-xl">
        <q-card class="col-md-5 col-sm-5 col-xs-10 column">
          <q-form @submit.prevent="onSubmit" class="q-gutter-md q-pa-lg">
            <q-select
              outlined
              v-model="form.civility"
              :options="civilityOption"
              label="Civilité"
              behavior="menu"
            />

            <div class="row justify-between q-gutter-y-md">
              <q-input
                v-model="form.firstName"
                outlined
                color="black"
                type="text"
                label="Nom *"
                clearable
                required
                class="col-md-5 col-sm-5 col-xs-12"
              />

              <q-input
                v-model="form.lastName"
                outlined
                color="black"
                type="text"
                label="Prénom *"
                clearable
                required
                class="col-md-5 col-sm-5 col-xs-12"
              />
            </div>
            <q-input
              v-model="form.organisation"
              outlined
              type="text"
              label="Nom ou raison sociale de l'entreprise demandeuse"
              hint="Mettez 'Particulier' si vous ne présentez pas une entreprise"
            />
            <!-- <div class="row justify-between"> -->
            <q-input
              v-model="form.email"
              color="black"
              type="email"
              label="Email"
              outlined
              class="col-md-5 col-sm-5 col-xs-12"
              clearable
            >
              <template v-slot:prepend>
                <q-icon name="mail" color="orange" />
              </template>
            </q-input>
            <q-input
              v-model="form.contact"
              color="black"
              outlined
              type="tel"
              label="Contact"
              class="col-md-5 col-sm-5 col-xs-12"
              clearable
            >
              <template v-slot:prepend>
                <q-icon name="phone" color="orange" />
              </template>
            </q-input>

            <q-input
              v-model="form.adresse"
              color="black"
              outlined
              type="text"
              label="adresse"
              class="col-md-5 col-sm-5 col-xs-12"
              clearable
            >
              <template v-slot:prepend>
                <q-icon name="place" color="orange" />
              </template>
            </q-input>

            <div class="row justify-between q-gutter-y-md">
              <q-input
                v-model="form.ville"
                outlined
                color="black"
                type="text"
                label="Ville"
                clearable
                required
                class="col-md-5 col-sm-5 col-xs-12"
              />

              <q-input
                v-model="form.region"
                outlined
                color="black"
                type="text"
                label="Etat/Département/Région"
                clearable
                required
                class="col-md-5 col-sm-5 col-xs-12"
              />
            </div>
            <q-select
              outlined
              v-model="form.pays"
              :options="options"
              label="Pays"
              behavior="menu"
            />
            <q-input
              v-model="form.services"
              outlined
              color="black"
              type="text"
              label="Service concerné*"
              clearable
              required
              class="col-md-6 col-sm-5 col-xs-12"
            />
            <!-- </div> -->

            <q-input
              v-model="form.message"
              outlined
              color="black"
              type="textarea"
              label="Demande *"
            />
            <!-- <div class=""> -->
            <ul class="q-mx-none q-my-lg text-body1">
              <li>
                Pour obtenir des devis précis, merci de fournir le plus
                d'informations possible...
              </li>
              <li>Les champs marqués d'un astérisque * sont obligatoires.</li>
              <li>
                Selon la nature des travaux à exécuter, votre devis vous sera
                fourni à l'adresse mail sous-indiqué dans un
              </li>
              <li>
                délai de 72 h au plus tard après la demande si toutes les
                informations utiles nous sont communiquées.
              </li>
              <li>
                Nous respectons votre vie privée. Vos coordonnées ne seront ni
                publiées, ni utilisées à des ﬁns personnelles.
              </li>
              <li>Consultez notre Politique de cookies.</li>
              <li>
                Ce site est protégé par reCAPTCHA et la Politique de
                conﬁdentialité et les Conditions d'utilisation de Google
                actuelles.
              </li>
            </ul>
            <!-- </div> -->
            <div class="row">
              <q-btn
                label="Envoyer"
                unelevated
                no-caps
                size="lg"
                padding="sm"
                class="col-md-4 col-sm-4 col-xs-12"
                type="submit"
                rounded
                color="amber-8"
              />
            </div>
          </q-form>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from "vue";
import { currencies } from "currencies.json";

const form = ref({});
const options = ref([]);
const civilityOption = ref(["", "Homme", "Femme"]);
// let data = {
//   service_id: process.env.SERVICE_ID,
//   template_id: process.env.TEMPLATE_ID,
//   user_id: process.env.TEMPLATE_ID.PUBLIC_KEY,
//   template_params: {
//     username: "James",
//     "g-recaptcha-response": "03AHJ_ASjnLA214KSNKFJAK12sfKASfehbmfd...",
//   },
// };
// emailjs
//   .sendForm(process.env.SERVICE_ID, process.env.TEMPLATE_ID, "#myForm")
//   .then(
//     (response) => {
//       console.log("SUCCESS!", response.status, response.text);
//     },
//     (error) => {
//       console.log("FAILED...", error);
//     }
//   );

defineOptions({
  name: "IndexPage",
});

const slide = ref("style");
const slideRealsation = ref(1);
currencies.map((currencie) => {
  options.value.push({ label: currencie.name, value: currencie.code });
});
const onSubmit = (event) => {
  //   event.preventDefault(); // prevent reload
  //   var formData = new FormData(this);
  //   formData.append("service_id", process.env.SERVICE_ID);
  //   formData.append("template_id", process.env.TEMPLATE_ID);
  //   formData.append("user_id", process.env.PUBLIC_KEY);
  //   fetch("https://api.emailjs.com/api/v1.0/email/send-form", {
  //     method: "POST",
  //     body: FormData,
  //   }).then((response) => {
  //     if (!response.ok) {
  //       throw new Error(`HTTP error! Status: ${response.status}`);
  //     }
  //     console.log("Response", response);
  //   });
};
</script>
