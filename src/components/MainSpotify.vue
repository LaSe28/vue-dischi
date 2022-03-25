<template>
  <main>
    <div v-if="arrSongs == null" class="text-white text-uppercase text-center">
      sto caricando i dati
      <div><i class="fas fa-spinner"></i></div>
    </div>
    <div v-else class="container">
      <div class="row justify-content-center">
        <SongsSpotify v-for="song in changedValue" :key="song.title"
        :img="song.poster"
        :song="song.title"
        :author="song.author"
        :date="song.year"/>
      </div>
    </div>
  </main>
</template>

<script>
import SongsSpotify from './SongsSpotify.vue'
import axios from 'axios'

export default {
  name: 'MainSpotify',
  components: {
    SongsSpotify
  },
  props: {
    valueGenChange: String,
    valueAutChange: String

  },
  data () {
    return {
      arrSongs: null
    }
  },
  computed: {
    changedValue () {
      if (this.valueAutChange === '') {
        return this.arrSongs.filter((objSongs) => objSongs.genre.toLowerCase().includes(this.valueGenChange.toLowerCase()))
      } else {
        return this.arrSongs.filter((objSongs1) => objSongs1.author.toLowerCase().includes(this.valueAutChange.toLowerCase()))
      }
    }
  },
  created () {
    setInterval(() => {
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((res) => {
          this.arrSongs = res.data.response
        })
    }, 3000)
  }
}
</script>

<style scoped lang="scss">
  main{
    min-height: calc(100vh - 5rem);
    background-color: #212D3A;
  }
  .fas{
    font-size: 3rem;
    animation-name: spin;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
  }
  @keyframes spin {
    25%{
      transform: rotate(90deg);
    }
    50%{
      transform: rotate(180deg);
    }
    75%{
      transform: rotate(270deg);
    }
    100%{
      transform: rotate(360deg);
    }
  }

</style>
