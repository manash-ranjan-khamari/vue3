<template>
  <div class="wrapper">
    <header class="main-head">VUE 3 CODE EXAMPLES</header>
    <nav class="main-nav">
        <ul>
            <li><img alt="Vue logo" src="./assets/logo.png" /></li>
            <li v-for="(item, index) in componentObj" :key="`example${index}`"><a :href="`#example${index}`">{{item.title}}</a></li> 
        </ul>
    </nav>
    <article class="content">
        <template v-for="(item, index) in componentObj">
          <h1 :id="`example${index}`">---- <u>{{item.title}}</u> ----</h1>
          <component :is="item.componentName" :message="item.message"/>
          <div class="space20"></div>
        </template>
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
import RefDemo from './components/Ref.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    PropsDemo,
    ComputedDemo,
    RefDemo
  },
  setup() {
    let componentObj = [{
      title: 'Basic Example',
      componentName: HelloWorld
    },
    {
      title: 'Props Example',
      componentName: PropsDemo,
      message: 'Hello there, I am Props data passed from parent'
    },
    {
      title: 'Computed Example',
      componentName: ComputedDemo
    },
    {
      title: 'Ref Example',
      componentName: RefDemo
    }];

    return {
      componentObj
    };
  }
}
</script>
