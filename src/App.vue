<template>
  <my-input placeholder="vstup"
            v-model:vysledek="myTitle"
  >
  </my-input >
  <my-button @click="showDialog1">otevřít dialog 1</my-button>
  <my-button @click="showDialog2">otevřít dialog 2</my-button>
  <my-dialog v-model:show="myDialog1Visible">
    <h2>Můj první dialog</h2>
  </my-dialog>
  <my-dialog v-model:show="myDialog2Visible">
    <h2>Můj druhý dialog</h2>
  </my-dialog>
  <h2>{{myTitle}}</h2>
</template>

<script>

export default {
  name: "App",
  data() {
    return {
      myDialog1Visible: false,
      myDialog2Visible: false,
      myTitle: ''
    }
  },
  methods: {
    showDialog1() {
      console.log("showDialog")
      this.myDialog1Visible = true
    },
    showDialog2() {
      console.log("showDialog")
      this.myDialog2Visible = true
    }
  }



}
</script>

<style scoped>

</style>