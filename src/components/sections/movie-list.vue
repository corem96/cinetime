<template>
  <div id="movie-list">
    <div v-for="movie in filteredMovies" :key="movie.id" class="movie">
      {{ movie.movie.Title }}
    </div>
  </div>
</template>

<script>
import Genres from '@/utils/genres'

  export default {
    // data() {
    //   return {
    //     // generos: Genres,
    //     movies: [
    //       { id:1 , title: 'Pulp Fiction', genre: Genres.CRIME },
    //       { id:2 , title: 'Blade Runner 2049', genre: Genres.SCIFI },
    //       { id:3 , title: 'Dunkirk', genre: Genres.WAR },
    //       { id:4 , title: 'Baby Driver', genre: Genres.ACTION }
    //     ]
    //   }
    // },
    props: ['genre', 'time', 'movies'],
    methods: {
      movieGenreFilter(movie) {
        if (!this.genre.length) {
          return true
        } else {
          return this.genre.find(genre => movie.genre === genre)
        }
      }
    },
    computed: {
      filteredMovies() {
        // return this.movies.filter(this.movieGenreFilter)
      }
    }
  }
</script>
