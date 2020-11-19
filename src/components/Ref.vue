<template>
    <h2>{{nameA}} works as a {{profession}}</h2>
    <button @click="switchName">Change name to {{nameB}}</button>
</template>

<script>
import {ref} from 'vue';

export default {
    setup() {
        let nameA = ref('Manash Khamari');
        let nameB = ref('Bill Gates');
        const profession = ref('IT Professional')
        
        const switchName = () => {
            [nameA.value, nameB.value] = [nameB.value, nameA.value];
        };

        return {
            nameA,
            nameB,
            profession,
            switchName
        };
    }
}
</script>