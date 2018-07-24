<template>
  <div id="app">
    <div id="title">
      <img src="./assets/logo.png">
      <router-view/>
    </div>

    <div id="overview">
      <div id="main" class="main">

        <!-- <movie-list v-bind:genre="genre" v-bind:time="time" v-bind:movies="movies"></movie-list> -->
        <movie-list v-bind:genre="genre" v-bind:time="time" ></movie-list>
        <movie-filter v-on:check-filter="checkFilter"></movie-filter>

      </div>
    </div>


  </div>
</template>

<script>
import movieList from '@/components/sections/movie-list'
import movieFilter from '@/components/sections/movie-filter'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    movieList,
    movieFilter
  },
  data() {
    return {
      genre: [],
      time: []
    }
  },
  methods: {
    checkFilter(category, title, state) {
      if(category) {
        this[category].push(title)
      } else {
        let index = this[category].indexOf(title)
        if (index > -1) {
          this[category].splice(index, 1)
        }
      }
    }
  },
  created () {
    axios.get('http://localhost:8080:api')
    .then(r => {
      console.log(res)
    })
  }
}
</script>

<style lang="scss"></style>
