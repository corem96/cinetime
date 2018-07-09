<template>
  <div id="app">
    <div id="title">
      <img src="./assets/logo.png">
      <router-view/>
    </div>

    <div id="overview">
      <div id="main" class="main">

        <movie-list></movie-list>
        <movie-filter v-on:check-filter="checkFilter"></movie-filter>

      </div>
    </div>


  </div>
</template>

<script>
import movieList from '@/components/sections/movie-list'
import movieFilter from '@/components/sections/movie-filter';

export default {
  name: 'App',
  components: {
    'movie-list': movieList,
    'movie-filter': movieFilter
  },
  methods: {
    checkFilter(cathegory, title, state) {

    }
  }
}
</script>

<style lang="scss"></style>
