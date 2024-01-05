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
  <!--<Events />
  <Computed />
  <Observers />-->
  <!--<LifeCicle />
  <Slots />
  <Slots>
    bbbbbbbbbbbbbbbb
    <template v-slot:title>Home</template>
    <template v-slot:description>odnsfu osudnfjwçpe oaskdn poqednu qufenpo upaounf</template>
    aaaaaaaaaaaaaaaa
  </Slots>-->
  <BaseCard/>
  <div class="card">Teste</div>
  <BaseAlert/>
  <BaseAlert variant="success"/>
</template> 

<script>
//import HelloWorld from './components/HelloWorld.vue';
import TheHeader from './components/TheHeader';
//import TwoWayDataBindingVue from './components/TwoWayDataBinding';
//import Events from './components/Events';
//import Computed from './components/Computed';
//import Observers from './components/Observers';
//import LifeCicle from './components/LifeCicle';
//import Slots from './components/Slots';
import BaseCard from './components/BaseCard';
import BaseAlert from './components/BaseAlert';

export default {
name: 'App',
aaa: false,
components: {
  //HelloWorld,
  TheHeader,
  //TwoWayDataBindingVue,
  //Events,
  //Computed,
  //Observers,
  //LifeCicle,
  //Slots,
  BaseCard,
  BaseAlert,
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
