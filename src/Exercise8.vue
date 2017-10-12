<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <h1>Exercise 8: Components</h1>
        <br>
        <button @click="selected='appBlue'" class="btn btn-primary">Blue</button>
        <button @click="selected='appGreen'" class="btn btn-success">Green</button>
        <button @click="selected='appRed'" class="btn btn-danger">Red</button>
        <hr>

          <component :is="selected"><h2>{{selected}}</h2></component>

      </div>
    </div>
  </div>
</template>

<script>
  import Blue from './components/Blue.vue'
  import Green from './components/Green.vue'
  import Red from './components/Red.vue'

  export default {
    components: {
      appBlue: Blue,
      appGreen: Green,
      appRed: Red,
    },
    data() {
      return {
        selected: '',
      };
    },
  };
</script>
