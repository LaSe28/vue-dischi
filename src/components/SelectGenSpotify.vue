<template>
    <select @change="value" name="" id="gen">
      <option value="">Seleziona Genere</option>
      <option value="Rock">Rock</option>
      <option value="Metal">Metal</option>
      <option value="Jazz">Jazz</option>
      <option value="Pop">Pop</option>
    </select>
</template>

<script>
export default {
  name: 'SelectGen',
  data () {
    return {
    }
  },
  methods: {
    value () {
      const genere = document.querySelector('#gen').value
      this.$emit('changeGen', genere)
    }
  }

}
</script>

<style lang="scss" scoped>
  select{
    margin: 0.5rem;
  }
</style>
