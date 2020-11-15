<template>
  <h1>{{ state.msg }}</h1>
</template>

<script>
import {reactive} from 'vue';
export default {
  name: 'HelloWorld',
  setup() {
    const state = reactive({
      msg: 'hello world'
    });

    return {state};
  }
}
</script>
