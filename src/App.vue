<template>
  <div class="container">
    <h1>Hello World</h1>
    <quote-grid :quotes="quotes"/>
  </div>
</template>

<script>
  import QuoteGrid from './components/QuoteGrid';
export default {
  name: 'app',
  components: {
    QuoteGrid,
  },
  data: () => ({
    quotes: [
            'You may say I\'m a dreamer;\n' +
            'But I\'m not the only one\n'
    ],
    maxQuotes: 10,
  }),
};
</script>

<style>
</style>
