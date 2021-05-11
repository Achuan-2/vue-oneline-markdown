<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <editor class="editor" ></editor>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import editor from './components/editor.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld,
    editor,
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
.editor {
  margin-top:50px;
}
</style>
