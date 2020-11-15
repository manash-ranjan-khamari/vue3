<template>
  <h2>{{ state.msg }}</h2>
</template>

<script>
import {reactive} from 'vue';
export default {
  name: 'HelloWorld',
  setup() {
    const state = reactive({
      msg: 'Hello world'
    });
    
    return {state};
  }
}
</script>
