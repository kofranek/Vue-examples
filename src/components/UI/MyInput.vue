<template>
  <input
      type="text"
      :value="vysledek"
      @input="updateInput"
  >

</template>

<script>
export default {
  name: "MyInput",
  props: {
    vysledek: [String,Number],
  },
  methods:{
    updateInput(event){
      console.log('event=',event.target.value)
      this.$emit('update:vysledek',event.target.value)
    }
  }
}
</script>

<style scoped>

</style>