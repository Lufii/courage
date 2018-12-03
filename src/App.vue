<template>
  <div id="app">
    <Quote theQuote="Press buttons"/>
    <CategoryButton quoteCategory='Courage' @clicked="onClickChild"></CategoryButton>
    <CategoryButton quoteCategory='Productivity' @clicked="onClickChild"></CategoryButton>
  </div>
</template>

<script>
import Quote from './components/Quote.vue'
import CategoryButton from './components/CategoryButton.vue'


export default {
  name: 'app',
  components: {
    Quote,
    CategoryButton
  },
  methods: {
    onClickChild (value) {
      console.log(value) // someValue
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
