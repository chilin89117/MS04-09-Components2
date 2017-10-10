<template>
  <div>
    <div class="title">
      <slot name="title"></slot>
      <span><slot name="subtitle">The Subtitle</slot></span>
    </div>
    <hr>
    <div class="quote">
      <slot name="content"></slot>
    </div>
  </div>
</template>

<script>
  export default {

  };
</script>

<style scoped>
  div {
    border: 1px solid #aaa;
    box-shadow: 2px 2px 5px black;
    padding: 30px;
    margin: 30px auto;
    text-align: center;
  }

  /* Styling in the child component is applied to data received in <slot> */
  h3 {
    color: red;
  }

  .title {
    font-style: italic;
  }
</style>
