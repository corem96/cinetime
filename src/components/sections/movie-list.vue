<template>
  <div id="movie-list">
    <div v-for="movie in movies" :key="movie.id" class="movie">
      {{ movie.title }}
    </div>
  </div>
</template>

<script>
import Genres from '@/utils/genres'

  export default {
    data() {
      return {
        generos: Genres,
        movies: [
          { id:1 , title: 'Pulp Fiction', genre: generos.CRIME },
          { id:2 , title: 'Blade Runner 2049', genre: generos.SCIFI },
          { id:3 , title: 'Dunkirk', genre: generos.WAR },
          { id:4 , title: 'Baby Driver', genre: generos.ACTION }
          // { id:1 , title: 'Pulp Fiction'},
          // { id:2 , title: 'Blade Runner 2049'},
          // { id:3 , title: 'Dunkirk'},
          // { id:4 , title: 'Baby Driver'},
        ]
      }
    },
    props: ['genre','time']
  }
</script>
