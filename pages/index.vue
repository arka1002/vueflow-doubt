<template>
    <div :class="style.container">
        <VueFlow v-model="elements" :style="{ backgroundColor: 'lightblue' }">
            <template #node-custom="props">
                <Card v-bind="props" />
            </template>
        </VueFlow>
    </div>
</template>
  
<script setup>
// https://nuxt.com/docs/guide/concepts/vuejs-development#composition-api
import { VueFlow } from '@vue-flow/core';
import { ref } from 'vue';
import Card from '../components/Card.vue';
import '~/node_modules/@vue-flow/core/dist/style.css'
import '~/node_modules/@vue-flow/core/dist/theme-default.css';
const elements = ref([
    {
        id: '1',
        type: 'custom',
        data: { name: 'QF1' },
        position: { x: 0, y: 0 },
    },
    {
        id: '2',
        type: 'custom',
        data: { name: 'QF2' },
        position: { x: 100, y: 0 },
    },
    {
        id: 'e1-2',
        source: '1',
        target: '2',
    },
]);
</script>

<style module="style">
.container {
    height: 100vh;
}
</style>
  