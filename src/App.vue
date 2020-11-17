<template>
  <div class="wrapper">
    <header class="main-head">VUE 3 CODE EXAMPLES</header>
    <nav class="main-nav">
        <ul>
            <li><img alt="Vue logo" src="./assets/logo.png" /></li>
            <li><a href="#example1">Hello World Example</a></li> 
            <li><a href="#example2">Props Example</a></li> 
            <li><a href="#example3">Computed Example</a></li>
        </ul>
    </nav>
    <article class="content">
        <h1 id="example1"><u>Example 1</u></h1>
        <HelloWorld />
        <div class="space20"></div>
        <h1 id="example2"><u>Example 2</u></h1>
        <PropsDemo message="Hello there, I am Props data passed from parent" />
        <div class="space20"></div>
        <h1 id="example3"><u>Example 3</u></h1>
        <ComputedDemo /> 
    </article> 
    <aside class="side"></aside>
    <div class="ad"></div>
    <footer class="main-footer">@MIT License, 2020</footer>
  </div>
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
