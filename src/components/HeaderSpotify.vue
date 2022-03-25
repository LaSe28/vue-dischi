<template>
  <header >
    <SelectGen @changeGen="changeGenDone"/>
    <SelectAuthor @changeAut="changeAutDone"/>
  </header>
</template>

<script>
import SelectGen from './SelectGenSpotify.vue'
import SelectAuthor from './SelectAuthorSpotify.vue'

export default {
  name: 'HeaderSpotify',
  components: {
    SelectGen,
    SelectAuthor
  },
  methods: {
    changeGenDone (valueGen) {
      this.$emit('changedGen', valueGen)
    },
    changeAutDone (valueAut) {
      this.$emit('changedAut', valueAut)
    }
  }
}
</script>

<style scoped lang="scss">
  header{
    height: 5rem;
    background-color: #303A45;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
