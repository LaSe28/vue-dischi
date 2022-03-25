<template>
  <div id="app">
    <HeaderSpotify @changedGen="selected"/>
    <MainSpotify :valueChange="valueSelected"/>
  </div>
</template>

<script>
import HeaderSpotify from './components/HeaderSpotify.vue'
import MainSpotify from './components/MainSpotify.vue'

export default {
  name: 'App',
  data () {
    return {
      valueSelected: ''
    }
  },
  components: {
    HeaderSpotify,
    MainSpotify
  },
  methods: {
    selected (valueSelected) {
      this.valueSelected = valueSelected
    }
  }
}
</script>

<style lang="scss">
@import '../node_modules/bootstrap/scss/bootstrap';
@import 'assets/styles/style.scss'

</style>
