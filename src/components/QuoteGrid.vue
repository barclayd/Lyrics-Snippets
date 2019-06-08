<template>
  <div class="row">
    <quote :key="index" @click.native="removeLyric(index)" v-for="(quote, index) in quotes">"{{ quote }}" </quote>
  </div>
</template>

<script>
import Quote from './Quote';
export default {
  name: 'QuoteGrid',
  props: ['quotes'],
  components: {
    Quote,
  },
  methods: {
    removeLyric(idx) {
      this.quotes.splice(idx, 1);
    }
  },
};
</script>

<style scoped></style>
