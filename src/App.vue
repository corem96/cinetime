<template>
  <div id="app">
    <img src="./assets/logo.png">

    <router-view/>

    <movie-list></movie-list>

  </div>
</template>

<script>
import movieList from '@/components/sections/movie-list'

export default {
  name: 'App',
  components: {
    'movie-list': movieList
  }
}
</script>

<style lang="scss"></style>
