<template>
    <div>
        <VueFlow v-model="elements" :style="{ backgroundColor: 'lightblue' }">
            <template #node-custom="props">
                <Card v-bind="props" />
            </template>
        </VueFlow>
    </div>
</template>


<script setup>
import { VueFlow } from '@vue-flow/core'
import { ref } from 'vue'
import Card from "../components/Card.vue"


const elements = ref([
    {
        id: '1',
        type: 'custom',
        data: { name: "QF1" },
        position: { x: 0, y: 0 },
    },
    {
        id: '2',
        type: 'custom',
        data: { name: "QF2" },
        position: { x: 100, y: 0 },
    },
    {
        id: 'e1-2',
        source: '1',
        target: '2',
    }
])

</script>