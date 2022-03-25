<template>
    <select @change="value" name="" id="aut">
      <option value="">Seleziona Autore</option>
      <option value="Bon Jovi">Bon Jovi</option>
      <option value="Iron Maiden">Iron Maiden</option>
      <option value="Queen">Queen</option>
      <option value="Michael Jacjson">Michael Jackson</option>
      <option value="Deep Purple">Deep Purple</option>
      <option value="Steve Gadd Band">Steve Gadd Band</option>
      <option value="Eric Clapton">Eric Clapton</option>
      <option value="Metallica">Metallica</option>
      <option value="Dave Weckl">Dave Weckl</option>
    </select>
</template>

<script>
export default {
  name: 'SelectAuthor',
  data () {
    return {
    }
  },
  methods: {
    value () {
      const autore = document.querySelector('#aut').value
      this.$emit('changeAut', autore)
    }
  }

}
</script>

<style lang="scss" scoped>
 select{
    margin: 0.5rem;
  }
</style>
