<template>
  <button type="button" v-on:click='onClickButton'>{{quoteCategory}}</button>
</template>

<script>
export default {
  name: 'CategoryButton',
  props: {
    quoteCategory: String
  },
  methods: {
    onClickButton () {
      this.$emit('clicked', this.quoteCategory)
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
