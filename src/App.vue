<template>
  <div class="container">
    <h1>Hello World</h1>
    <new-quote @quoteAdded="newQuote" />
    <quote-grid :quotes="quotes" />
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

<style></style>
