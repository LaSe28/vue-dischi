<template>
    <select @change="value" name="" id="gen">
      <option value="">Tutti</option>
      <option value="Rock">Rock</option>
      <option value="Metal">Metal</option>
      <option value="Jazz">Jazz</option>
      <option value="Pop">Pop</option>
    </select>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  methods: {
    value () {
      const valueChose = document.querySelector('#gen').value
      this.$emit('change', valueChose)
    }
  }

}
</script>

<style lang="scss" scoped>
  select{
        margin-right: 20rem;
      }
</style>
