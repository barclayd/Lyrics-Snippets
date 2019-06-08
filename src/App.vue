<template>
  <div class="container">
    <new-quote @quoteAdded="newQuote" />
    <quote-grid :quotes="quotes" />
    <div class="row info">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info" role="alert">
          Click on a lyric to remove it
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid';
import NewQuote from './components/NewQuote';
export default {
  name: 'app',
  components: {
    QuoteGrid,
    NewQuote,
  },
  data: () => ({
    quotes: ["You may say I'm a dreamer;\n" + "But I'm not the only one"],
    maxQuotes: 10,
  }),
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    },
  },
};
</script>

<style scoped>
  .info {
    margin: 20px;
  }
</style>
