<template>
  <div class="hello">
    <h1>{{ theQuote }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Quote',
  props: {
    theQuote: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
