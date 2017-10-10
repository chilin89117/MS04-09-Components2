<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <br>
        <button @click="selected='appQuote'">Quote</button>
        <button @click="selected='appAuthor'">Author</button>
        <button @click="selected='appNew'">New</button>
        <hr>

        <!-- Dynamic component with <keep-alive> to prevent 'destroyed()' -->
        <keep-alive>
          <component :is="selected"></component>
        </keep-alive>

          <!-- <appQuote> -->
            <!-- Split data into 2 named slots -->
            <!-- Default: elements with no slots go to un-named <slot> -->
            <!-- <h3 slot="title">{{quoteTitle}}</h3> -->
            <!-- <p slot="content">{{quote}}</p> -->
          <!-- </appQuote> -->

      </div>
    </div>
  </div>
</template>

<script>
  import Quote from './components/Quote.vue'
  import Author from './components/Author.vue'
  import New from './components/New.vue'

  export default {
    data() {
      return {
        quoteTitle: 'The Quote',
        quote: 'To be or not to be...',
        selected: 'appQuote',   // Default component
      };
    },
    components: {
      appQuote: Quote,
      appAuthor: Author,
      appNew: New,
    },
  };
</script>

<style scoped>
  h3 {
    color: blue;
  }
</style>
