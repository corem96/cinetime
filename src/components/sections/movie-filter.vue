<template>
  <div id="movie-filter">
    <h2>Filter results</h2>
    <div class="filter-group">
      <check-filter v-for="genre in genres" :key="genre"></check-filter>
      <!-- <check-filter v-bind="genres"></check-filter> -->
    </div>
  </div>
</template>

<script>
import checkFilter from '@/components/check-filter';
import Genres from '@/utils/genres'

  export default {
    components: {
      'check-filter': checkFilter
    },
    data () {
      return {
        genres: Genres
      }
    }
  }
</script>
