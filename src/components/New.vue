<template>
  <div>
    <h4>New Component</h4>
    <br><br>
    <button @click="counter++">Counter++</button>
    <br><br>
    <p>Counter: {{counter}}</p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        counter: 0,
      };
    },
    destroyed() {
      console.log('"New" component destroyed!');
    },
    // When component is kept alive, it has 'activated' and 'deactivated' hooks
    activated() {
      console.log('"New" component activated.');
    },
    deactivated() {
      console.log('"New" component deactivated.');
    },
  };
</script>

<style scoped>
</style>
