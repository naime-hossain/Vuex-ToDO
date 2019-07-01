<template>
  <div id="app">
    <AddToDo />
    <to-dos></to-dos>
  </div>
</template>

<script>
import ToDos from "./components/ToDos";
import AddToDo from "./components/AddToDo";

export default {
  name: "app",
  components: {
    ToDos,
    AddToDo
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
