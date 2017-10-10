<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <appQuote>
          <!-- Split data into 2 named slots -->
          <!-- Default: elements with no slots go to un-named <slot> -->
          <h3 slot="title">{{quoteTitle}}</h3>
          <p slot="content">{{quote}}</p>
        </appQuote>
      </div>
    </div>
  </div>
</template>

<script>
  import Quote from './components/Quote.vue'

  export default {
    data() {
      return {
        quoteTitle: 'The Quote',
        quote: 'To be or not to be...',
      };
    },
    components: {
      appQuote: Quote,
    },
  };
</script>

<style scoped>
  h3 {
    color: blue;
  }
</style>
