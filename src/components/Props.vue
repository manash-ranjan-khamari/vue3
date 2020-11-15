<template>
    <h2><i>{{ state.msg }}</i></h2>
</template>

<script>
import {reactive} from 'vue';

export default {
    setup(props) {
        const state = reactive({
            msg: props.message
        });

        return {state};
    },
    props: {
        message: String
    }
}
</script>