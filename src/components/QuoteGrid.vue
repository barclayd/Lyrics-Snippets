<template>
  <div class="row">
    <quote :key="index" v-for="(quote, index) in quotes">
      {{ quote }}
    </quote>
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
};
</script>

<style scoped></style>
