<template>
  <div class="row">
    <div class="card">
      <img :src="img" alt="">
      <h4>{{song}}</h4>
      <div>{{author}}</div>
      <div>{{date}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SongsSpotify',
  props: {
    song: String,
    img: String,
    author: String,
    date: String
  }
}

</script>

<style scoped lang="scss">

.card{
  text-align: center;
  color: grey;
  width: 200px;
  margin: 1rem;
  background-color: #303A45;
  img{
    width: 100%;
    padding: 1rem;
  }
  h4{
    color: white;
    text-transform: uppercase;
  }
}

</style>
