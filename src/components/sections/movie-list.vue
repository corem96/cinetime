<template>
  <div id="movie-list">
    <div v-for="movie in movies" :key="movie.id" class="movie">
      {{ movie.title }}
    </div>
  </div>
</template>

<script>
  export default {
    data: () => {
      return {
        movies: [
          { id:1 , title: 'Pulp Fiction' },
          { id:2 , title: 'Blade Runner 2049' },
          { id:3 , title: 'Dunkirk' },
          { id:4 , title: 'Baby Driver' },
        ]
      }
    }
  }
</script>
