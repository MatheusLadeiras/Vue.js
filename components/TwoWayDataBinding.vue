<template>
    <div>
        One-way data binding <br>
        Two-way data binding <br>
        v-model -> formulários
    </div>

    <input v-model="name" type="text">
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue';
import TheHeader from './components/TheHeader';

export default {
  name: 'App',
  data() {
    return {
      name: 'jon Snow'
    }
  }
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