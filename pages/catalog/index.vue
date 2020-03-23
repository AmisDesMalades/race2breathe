<template>
  <main role="main">
    <section class="jumbotron text-center">
      <div class="container">
        <h1>Catalogue</h1>
        <p class="lead text-muted">
          Choisisez l'équipement que vous voulez et nous trouverons des
          volontaires locaux pour le produire et le faire parvenir rapidement.
        </p>
        <!-- <p>
          <a href="#" class="btn btn-primary my-2">Main call to action</a>
          <a href="#" class="btn btn-secondary my-2">Secondary action</a>
        </p> -->
      </div>
    </section>

    <div class="album py-5 bg-light">
      <div class="container">
        <h1>Protection des soignants</h1>
        <p class="lead text-muted">
          Nous avons sélectionné les meilleurs modèles de matériel libre de
          protection disponible.
        </p>
        <div class="row">
          <div class="col-md-12">
            <!-- VISIERE -->
            <b-card
              title="Visières"
              sub-title="PRUSA RC2"
              img-src="~assets/visiere-prusa.png"
              img-alt="Visière Prusa"
              img-right
              img-width="600"
              tag="article"
              class="mb-2"
            >
              <b-card-text>
                Pour éviter les projections contaminantes par les patients. Les
                autres personnes exposées comme les médecins de ville,
                caissiers, etc. pourraient également bénéficier de ces visières.
              </b-card-text>
              <b-form-select
                v-model="selected"
                :options="options"
              ></b-form-select>
              <b-button href="#" variant="primary">+</b-button>
            </b-card>
          </div>
          <div class="col-md-12">
            <!-- MASQUE -->
            <b-card
              title="Masques FPP2"
              sub-title="Open Source Mask"
              img-src="~assets/masque-copper-2.png"
              img-alt="Masque Open Source Mask"
              img-right
              img-width="600"
              tag="article"
              class="mb-2"
            >
              <b-card-text>
                Pour éviter les projections contaminantes par les patients. Les
                autres personnes exposées comme les médecins de ville,
                caissiers, etc. pourraient également bénéficier de ces visières.
              </b-card-text>
              <b-form-select
                v-model="selected"
                :options="options"
              ></b-form-select>
              <b-button href="#" variant="primary">+</b-button>
            </b-card>
            <!-- Ouverture de porte -->
            <b-card
              title="Poignée sans contact"
              sub-title="Ajout de poignée"
              img-src="~assets/door-opener.png"
              img-alt="Masque Open Source Mask"
              img-right
              img-width="600"
              tag="article"
              class="mb-2"
            >
              <b-card-text>
                Pour éviter les projections contaminantes par les patients. Les
                autres personnes exposées comme les médecins de ville,
                caissiers, etc. pourraient également bénéficier de ces visières.
              </b-card-text>
              <b-form-select
                v-model="selected"
                :options="options"
              ></b-form-select>
              <b-button href="#" variant="primary">+</b-button>
            </b-card>
          </div>
        </div>

        <h1>Equipement de ventilation de crise</h1>
        <p class="lead text-muted">
          Modèles de ventilation d'urgence.
        </p>
        <div class="row">
          <div class="col-md-12">
            <!-- VISIERE -->
            <b-card
              title="Respirateur d'urgence"
              sub-title="Open Lung"
              img-src="~assets/respirateur-openlung.png"
              img-alt="Open Lung"
              img-right
              img-height="200"
              tag="article"
              class="mb-2"
            >
              <b-card-text>
                Un projet avancé qui transforme un ambubag de ventilation manuel
                en respirateur automatisé.
              </b-card-text>
              <b-form-select
                v-model="selected"
                :options="options"
              ></b-form-select>
              <b-button href="#" variant="primary">+</b-button>
            </b-card>
          </div>
          <div class="col-md-12">
            <!-- MASQUE -->
            <b-card
              title="Valve de dédoublement"
              sub-title="Impression 3D"
              img-src="~assets/valve-triple.png"
              img-alt="Valve triple"
              img-right
              img-width="600"
              tag="article"
              class="mb-2"
            >
              <b-card-text>
                Pour éviter les projections contaminantes par les patients. Les
                autres personnes exposées comme les médecins de ville,
                caissiers, etc. pourraient également bénéficier de ces visières.
              </b-card-text>
              <b-form-select
                v-model="selected"
                :options="options"
              ></b-form-select>
              <b-button href="#" variant="primary">+</b-button>
            </b-card>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  components: {},
  data() {
    return {
      selected: null,
      options: [
        { value: null, text: 'Please select an option' },
        { value: 'a', text: 'This is First option' },
        { value: 'b', text: 'Selected Option' },
        { value: { C: '3PO' }, text: 'This is an option with object value' },
        { value: 'd', text: 'This one is disabled', disabled: true }
      ]
    }
  }
})
</script>

<style lang="sass" scoped></style>
