<template>
    <div>
        <!-- <VueFlow v-model="elements" :style="{ backgroundColor: 'lightblue' }">
            <template #node-custom="props">
                <Card v-bind="props" />
            </template>
        </VueFlow> -->
        <Random/>
    </div>
</template>


<script setup>
import { ref } from 'vue'
import { geometry, Image, Surface, Path, Text, Group } from '@progress/kendo-drawing';
const { Rect, Point, Size, transform } = geometry;
import Random from "../components/Random.vue";

const path = new Path({
    stroke: {
        color: "#9999b6",
        width: 2
    }
});


</script>