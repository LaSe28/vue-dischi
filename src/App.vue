<template>
  <div id="app">
    <HeaderSpotify @changedGen="selectedGen" @changedAut="selectedAut"/>
    <MainSpotify :valueGenChange="valueGenSelected"
    :valueAutChange="valueAutSelected"
    />
  </div>
</template>

<script>
import HeaderSpotify from './components/HeaderSpotify.vue'
import MainSpotify from './components/MainSpotify.vue'

export default {
  name: 'App',
  data () {
    return {
      valueGenSelected: '',
      valueAutSelected: ''
    }
  },
  components: {
    HeaderSpotify,
    MainSpotify
  },
  methods: {
    selectedGen (valueGenSelected) {
      this.valueGenSelected = valueGenSelected
    },
    selectedAut (valueAutSelected) {
      this.valueAutSelected = valueAutSelected
    }
  }
}
</script>

<style lang="scss">
@import '../node_modules/bootstrap/scss/bootstrap';
@import 'assets/styles/style.scss'

</style>
