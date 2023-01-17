<template>
<h1>{{ count }}</h1>
<button @click="increase" style="font-size:3rem;padding:2rem">+</button>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      count:1
    }
  },
  methods: {
    increase: function() {
      this.count++;
      androidApp.toastText("Hi from Vue.js");
    }
  },
  mounted() {
    document.addEventListener("vueIncrease", this.increase);
  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
