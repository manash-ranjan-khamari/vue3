<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>
    <a href="#example1">Hello World Example</a>, 
    <a href="#example2">Props Example</a>
    <a href="#example3">Computed Example</a> 
  </div>
  <hr>
  <h1 id="example1"><u>Example 1</u></h1>
  <HelloWorld />
  <hr >
  <h1 id="example2"><u>Example 2</u></h1>
  <PropsDemo message="Hello there, I am Props data passed from parent" />
  <hr>
  <h1 id="example3"><u>Example 3</u></h1>
  <ComputedDemo /> 
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import PropsDemo from './components/Props.vue';
import ComputedDemo from './components/Computed.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    PropsDemo,
    ComputedDemo
  }
}
</script>
