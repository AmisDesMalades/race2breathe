/* eslint-disable camelcase */ /* eslint-disable camelcase */
<template>
  <main role="main">
    <section class="jumbotron text-center">
      <div class="container">
        <h1>Simulation</h1>
        <p class="lead text-muted">
          Simulation de production des éléments de protection des soignants
          imprimés en 3D.
        </p>
      </div>
    </section>

    <div class="album py-5 bg-light">
      <div class="container">
        <h1>Protection des soignants</h1>
        <p class="lead text-muted">
          Nous avons sélectionné et validé médicalement cette visière de
          protection également validé par le ministrère de la santé tchèque.
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
            </b-card>
          </div>
        </div>

        <b-form @submit="onSubmit" @reset="onReset">
          <hr />
          <div class="row">
            <div class="col-md-12">
              <h3>Achat d'imprimantes</h3>
              <b-form-group
                label-cols="4"
                label-cols-lg="4"
                label-size="lg"
                label="Quantité d'imprimante"
                label-for="input-lg"
              >
                <b-form-input
                  id="quantite_imprimante"
                  v-model="quantite_imprimante"
                  size="lg"
                  type="number"
                ></b-form-input>
              </b-form-group>

              <b-form-group
                label-cols="4"
                label-cols-lg="4"
                label-size="lg"
                label="Prix par imprimante"
                label-for="input-lg"
              >
                <b-form-input
                  id="prix_imprimante"
                  v-model="prix_imprimante"
                  size="lg"
                  type="number"
                ></b-form-input>
              </b-form-group>

              <b-form-group
                label-cols="4"
                label-cols-lg="4"
                label-size="lg"
                label="Capacité production / jour / imprimante"
                label-for="input-lg"
              >
                <b-form-input
                  id="capacite_journaliere"
                  v-model="capacite_journaliere"
                  size="lg"
                  type="number"
                ></b-form-input>
              </b-form-group>
            </div>
          </div>

          <hr />
          <div class="row">
            <div class="col-md-12">
              <h3>Consommables 3D par visière</h3>
              <div>
                <b-form-group
                  label-cols="4"
                  label-cols-lg="4"
                  label-size="lg"
                  label="Poids en plastique (en g)"
                  label-for="input-lg"
                >
                  <b-form-input
                    id="poids_visiere"
                    v-model="poids_visiere"
                    size="lg"
                    type="number"
                    step=".01"
                  ></b-form-input>
                </b-form-group>

                <b-form-group
                  label-cols="4"
                  label-cols-lg="4"
                  label-size="lg"
                  label="Prix du plastique (en g)"
                  label-for="input-lg"
                >
                  <b-form-input
                    id="prix_plastique"
                    v-model="prix_plastique"
                    size="lg"
                    type="number"
                    step=".01"
                  ></b-form-input>
                </b-form-group>
              </div>
            </div>
          </div>

          <hr />
          <div class="row">
            <div class="col-md-12">
              <h3>Eléments externes par visière</h3>
              <ul>
                <li>
                  1 x Feuille de plastique transparent rigide 0.3mm
                </li>
                <li>
                  1 x Revêtement silicone
                </li>
                <li>
                  1 x Bande élastique
                </li>
                <li>
                  1 x Pochette plastique d'emballage
                </li>
              </ul>
              <b-form-group
                label-cols="4"
                label-cols-lg="4"
                label-size="lg"
                label="Prix par feuille de plastique"
                label-for="input-lg"
              >
                <b-form-input
                  id="prix_feuille"
                  v-model="prix_feuille"
                  size="lg"
                  type="number"
                  step=".01"
                ></b-form-input>
              </b-form-group>

              <b-form-group
                label-cols="4"
                label-cols-lg="4"
                label-size="lg"
                label="Prix par bande élastique"
                label-for="input-lg"
              >
                <b-form-input
                  id="prix_bande"
                  v-model="prix_bande"
                  size="lg"
                  type="number"
                  step=".01"
                ></b-form-input>
              </b-form-group>

              <b-form-group
                label-cols="4"
                label-cols-lg="4"
                label-size="lg"
                label="Prix par revêtement silicone"
                label-for="input-lg"
              >
                <b-form-input
                  id="prix_silicone"
                  v-model="prix_silicone"
                  size="lg"
                  type="number"
                  step=".01"
                ></b-form-input>
              </b-form-group>

              <b-form-group
                label-cols="4"
                label-cols-lg="4"
                label-size="lg"
                label="Prix par emballage"
                label-for="input-lg"
              >
                <b-form-input
                  id="prix_emballage"
                  v-model="prix_emballage"
                  size="lg"
                  type="number"
                  step=".01"
                ></b-form-input>
              </b-form-group>
            </div>
          </div>

          <hr />
          <div class="row">
            <div class="col-md-12">
              <h3>Autres coûts</h3>
              <div>
                <b-form-group
                  label-cols="4"
                  label-cols-lg="4"
                  label-size="lg"
                  label="Frais supplémentaires"
                  label-for="input-lg"
                >
                  <b-form-input
                    id="prix_autres"
                    v-model="prix_autres"
                    size="lg"
                    type="number"
                    step=".01"
                  ></b-form-input>
                </b-form-group>
              </div>
            </div>
          </div>
          <b-button type="submit" variant="primary">Calculer</b-button>
          <b-button type="reset" variant="danger">Reset</b-button>
        </b-form>

        <b-card class="mt-3" header="Résultats">
          <h2>
            Coût par visière:
            <span id="prix_visiere">{{ prix_par_unite_total }}€</span>
          </h2>
          <h2>
            Production journalière:
            <span id="quantite_production">{{
              capacite_journaliere_totale
            }}</span>
          </h2>
          <h2>
            Production hebdomadaire:
            <span id="quantite_production">{{
              capacite_journaliere_totale * 7
            }}</span>
          </h2>
          <h2>
            Production mensuelle:
            <span id="quantite_production">{{
              capacite_journaliere_totale * 30
            }}</span>
          </h2>
          <h2>
            Coût total:
            <span id="prix_visiere">{{ prix_total }}€</span>
          </h2>
          <!-- <pre class="m-0">{{ form }}</pre> -->
        </b-card>
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
      quantite_imprimante: 10,
      prix_imprimante: 750,
      poids_visiere: 50,
      prix_plastique: 0.02,
      capacite_journaliere: 8,
      prix_feuille: 0.1,
      prix_bande: 0.2,
      prix_silicone: 0.5,
      prix_emballage: 0,
      prix_autres: 0,

      total_imprimantes: 0,
      prix_par_unite_3d: 0,
      prix_par_unite_total: 0,
      capacite_journaliere_totale: 0,
      prix_total: 0,

      show: true
    }
  },
  methods: {
    onSubmit(evt: any) {
      evt.preventDefault()
      this.calculPrix()
    },
    mounted() {
      this.calculPrix()
    },
    calculPrix() {
      this.total_imprimantes = this.quantite_imprimante * this.prix_imprimante
      this.prix_par_unite_3d = this.prix_plastique * this.poids_visiere
      this.prix_par_unite_total =
        this.prix_par_unite_3d +
        this.prix_feuille +
        this.prix_silicone +
        this.prix_bande +
        this.prix_emballage
      this.capacite_journaliere_totale =
        this.quantite_imprimante * this.capacite_journaliere
      this.prix_total =
        this.total_imprimantes +
        this.capacite_journaliere_totale * this.prix_par_unite_total
    },
    onReset(evt: any) {
      evt.preventDefault()
      // Reset our form values
      this.quantite_imprimante = 100
      this.prix_imprimante = 750
      this.poids_visiere = 32
      this.prix_plastique = 0.02
      this.capacite_journaliere = 6
      this.prix_feuille = 0.1
      this.prix_bande = 0.2
      this.prix_silicone = 0.5
      this.prix_emballage = 0
      this.prix_autres = 0
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
})
</script>

<style lang="sass" scoped></style>
