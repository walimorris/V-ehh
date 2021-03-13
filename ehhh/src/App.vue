<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld/>
    <Component1/>
    <Component2/>
    <Component3/>
    <ClickModal/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Component1 from './components/Component1.vue';
import Component2 from './components/Component2.vue';
import Component3 from './components/Component3.vue';
import ClickModal from './components/ClickModal.vue';

export default {
  name: 'App',
  components: {
    ClickModal,
    HelloWorld,
    Component1,
    Component2,
    Component3,
  },
};
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
