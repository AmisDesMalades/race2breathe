<template>
  <div class="container">
    <div>
      <img src="~/assets/logo.jpg" alt="RACE 2 BREATHE" height="400" />
      <h1 class="title">
        RACE 2 BREATHE
      </h1>
      <h2 class="subtitle">
        Logistic platform linking hospital PPE demands with local 3d printing
        production for the COVID-19 crisis.
        <br />
      </h2>
      <div class="links">
        <b-link href="./simulation">
          <b-button variant="info" size="lg">Simulation</b-button>
        </b-link>
        <!-- <b-button variant="primary" size="lg">Volunteer 3D</b-button> -->
        <!-- <b-button variant="info" size="lg">Hospital</b-button> -->
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  components: {}
})
</script>

<style lang="scss" scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
