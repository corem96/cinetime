<template>
  <div id="movie-filter">
    <h2>Filter results</h2>
    <div class="filter-group">
      <check-filter v-for="genre in genres" :key="genre" v-bind:title="genre" v-on:check-filter="checkFilter"></check-filter>
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
    },
    methods: {
      checkFilter(cathegory, title, state) {
        this.$emit('check-filter', cathegory, title, state)
      }
    }
  }
</script>
