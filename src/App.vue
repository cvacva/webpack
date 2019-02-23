<template>
  <div id="app">
    <img src="./assets/logo.png">
    <!-- <HelloWorld/> -->
    <!-- <Event/> -->
    <!-- <formdata/> -->
    <!-- <styleClass/> -->
    <!-- <myComponents/> -->
    <!-- <father/> -->
    <!-- <parent/> -->
    <abc/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Event from './components/Event'
import formdata from './components/formdata'
import styleClass from './components/styleClass'
import myComponents from './components/myComponents'
import father from './components/father'
import parent from './components/slots/parent'
import abc from './components/comkeep/big'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Event,
    formdata,
    styleClass,
    myComponents,
    father,
    parent,
    abc
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
