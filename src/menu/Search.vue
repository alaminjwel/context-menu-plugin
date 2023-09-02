<template lang="pug">
.search
  input(v-model="value")
</template>

<script>
export default {
  props: ['value', 'search'],
  watch: {
    value() {
      this.$emit('search', this.value);
    }
  }
}
</script>


<style lang="sass" scoped>
.search
  input    
    color: red
    padding: 1px 8px
    border: 3px solid red
    border-radius: 10px
    font-size: 16px
    font-family: serif
    width: 100%
    box-sizing: border-box
    background: transparent
</style>
