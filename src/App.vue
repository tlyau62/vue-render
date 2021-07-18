<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <List v-model="data" />
    {{ data }}
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import List from "./components/List";

export default {
  name: "App",
  components: {
    HelloWorld,
    List,
  },
  data() {
    return {
      data: {
        field1: "1",
        field2: "2",
        field3: "3",
      },
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
