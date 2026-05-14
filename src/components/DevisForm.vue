<template>
  <div class="bg-lime-1 q-py-lg" id="devis">
    <div class="row justify-center q-my-md q-px-xl">
      <q-separator spaced inset size=".5rem" color="black" class="col-1" />
    </div>
    <p class="text-h5 text-black text-center q-px-lg">
      Vous avez un projet immobilier à Abidjan, en Côte d'Ivoire ou dans la
      sous-région ? Nous avons l'expertise pour le réaliser au-delà de vos
      espérances ! Nombreux sont ceux qui nous sollicitent chaque jour et qui
      repartent satisfaits.
    </p>
    <p class="text-h5 text-black text-center q-px-lg">
      Soumettez-nous simplement votre demande pour obtenir un devis estimatif
      détaillé de votre projet. Nous sommes déjà ravis de commencer avec vous
      une nouvelle collaboration à succès !
    </p>
    <p class="text-h4 text-weight-bolder text-black text-center q-pa-lg">
      FORMULAIRE DE DEMANDE DE DEVIS
    </p>
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
            label="Adresse"
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
            :options="countryOptions"
            label="Pays"
            behavior="menu"
          />
          <q-input
            v-model="form.services"
            outlined
            color="black"
            type="text"
            label="Service concerné *"
            clearable
            required
            class="col-md-6 col-sm-5 col-xs-12"
          />
          <q-input
            v-model="form.message"
            outlined
            color="black"
            type="textarea"
            label="Demande *"
          />
          <ul class="q-mx-none q-my-lg text-body1">
            <li>
              Pour obtenir des devis précis, merci de fournir le plus
              d'informations possible...
            </li>
            <li>Les champs marqués d'un astérisque * sont obligatoires.</li>
            <li>
              Selon la nature des travaux à exécuter, votre devis vous sera
              fourni à l'adresse mail sous-indiqué dans un délai de 72 h au
              plus tard après la demande si toutes les informations utiles nous
              sont communiquées.
            </li>
            <li>
              Nous respectons votre vie privée. Vos coordonnées ne seront ni
              publiées, ni utilisées à des fins personnelles.
            </li>
            <li>Consultez notre Politique de cookies.</li>
            <li>
              Ce site est protégé par reCAPTCHA et la Politique de
              confidentialité et les Conditions d'utilisation de Google
              actuelles.
            </li>
          </ul>
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
</template>

<script setup>
import { ref } from "vue";
import { currencies } from "currencies.json";

const form = ref({});
const civilityOption = ["", "Homme", "Femme"];
const countryOptions = currencies.map((c) => ({ label: c.name, value: c.code }));

const onSubmit = () => {};
</script>
