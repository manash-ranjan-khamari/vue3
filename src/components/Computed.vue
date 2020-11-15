<template>
    <h2>Number is {{state.count}}, double value is {{state.doubleVal}}</h2> 
    <button @click="state.count++">Increment</button>
</template>

<script>
import { computed, reactive } from 'vue'
export default {
    setup() {
        const state = reactive({
            count: 0,
            doubleVal: computed(() => state.count * 2)
        });

        return {state};
    }
}
</script>