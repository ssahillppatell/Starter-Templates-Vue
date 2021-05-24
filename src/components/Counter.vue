<template>
    <h3>Counter</h3>
    <h5>{{ state.count }} * 2 = {{ times2 }}</h5>
    <button @click="inc(1)">Increment</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import store from '../store';

export default defineComponent({
    name: 'Counter',
    setup() {
        const { state, times2, inc } = store;
        return {
            state,
            times2,
            inc,
        };
    },
});
</script>
