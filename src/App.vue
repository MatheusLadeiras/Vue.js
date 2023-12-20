<template>
    <TheHeader v-if="showHeader"/>
    <div v-show="showName">
      Nome:      {{ firstName }} <br>
      Sobrenome: {{ lastName }}
    </div>
    <div v-if="acessLevel === 'admin'">Acesso Admin</div>
    <div v-else-if="acessLevel === 'marketing'">Acesso Marketing</div>
    <div v-else>User</div>
    <img alt="Vue logo" src="./assets/logo.png">
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <!--<TwoWayDataBindingVue />-->
    <Events />
    <Computed />
</template> 

<script>
//import HelloWorld from './components/HelloWorld.vue';
import TheHeader from './components/TheHeader';
//import TwoWayDataBindingVue from './components/TwoWayDataBinding';
import Events from './components/Events';
import Computed from './components/Computed'

export default {
  name: 'App',
  aaa: false,
  components: {
    //HelloWorld,
    TheHeader,
    //TwoWayDataBindingVue,
    Events,
    Computed,
  },
  data() {
    return {
      showHeader: false, //Choose in "true" to show the "TheHeader"
      firstName: 'Jon',
      lastName: 'Snow',
      showName: false,
      acessLevel: 'marketing',
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
