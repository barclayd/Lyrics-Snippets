<template>
  <div class="container">
    <progress-bar :percentage="(this.quotes.length / maxQuotes) * 100" />
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
import ProgressBar from './components/ProgressBar';

export default {
  name: 'app',
  components: {
    QuoteGrid,
    NewQuote,
    ProgressBar,
  },
  data: () => ({
    quotes: ["You may say I'm a dreamer;\n" + "But I'm not the only one"],
    maxQuotes: 10,
  }),
  methods: {
    newQuote(quote) {
      if (this.quotes.length < this.maxQuotes) {
        this.quotes.push(quote);
      } else {
        alert(
          'Max number of lyrics added!\nPlease remove one before adding a new lyric snippet',
        );
      }
    },
  },
};
</script>

<style scoped>
.info {
  margin: 20px;
}
</style>
