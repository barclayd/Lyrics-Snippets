<template>
  <form>
    <div class="form-group row new-quote">
      <div class="col-sm-12 text-center">
        <h4>Enter a favourite lyric</h4>
      </div>
    </div>
    <div class="form-group row new-quote">
      <label for="quote" class="col-sm-2 col-form-label">Quote</label>
      <div class="col-sm-10">
        <textarea
          @keyup.enter="createNew"
          class="form-control"
          id="quote"
          rows="3"
          v-model="quote"
        ></textarea>
      </div>
    </div>
    <div class="form-group row new-quote">
      <div class="col-sm-8">
        <button class="btn btn-primary" @click.prevent="createNew">
          Add Quote
        </button>
      </div>
    </div>
  </form>
</template>

<script>
export default {
  data: () => ({
    quote: '',
  }),
  methods: {
    createNew() {
      if (this.quote.trim().length > 0) {
        this.$emit('quoteAdded', this.quote);
        this.quote = '';
      }
    },
  },
};
</script>

<style scoped>
  .new-quote {
    margin-left: 50px !important;
  }
</style>
