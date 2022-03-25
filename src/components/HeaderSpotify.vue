<template>
  <header >
    <SelectGen @change="changeDone"/>
  </header>
</template>

<script>
import SelectGen from './SelectGenSpotify.vue'

export default {
  name: 'HeaderSpotify',
  components: {
    SelectGen
  },
  methods: {
    changeDone (value) {
      this.$emit('changedGen', value)
    }
  }
}
</script>

<style scoped lang="scss">
  header{
    height: 5rem;
    background-color: #303A45;
    display: flex;
    justify-content: end;
    align-items: center;
  }
</style>
