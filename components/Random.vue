<template>
    <svg :width="width" :height="height" viewBox="0 0 100 100" version="1.1" xmlns="http://www.w3.org/2000/svg">

        <polyline points="0 0 50 0 50 50 100 50 50 50 50 100 0 100" stroke="orange" fill="transparent"
            stroke-width="5" />
    </svg>
</template>


<script setup>

import { computed } from 'vue';


const props = defineProps(["height", "width"]);


const myFinalPath = computed(() => {
    const height = props.height;
    const width = props.width;

    const polyWidth = Number(width) / 2;
    const polyHeight = Number(height) / 2;

    const polyLinePoints = `0 0 ${polyWidth} 0 ${polyWidth} ${polyHeight} ${polyWidth * 2} ${polyHeight} ${polyWidth} ${polyHeight} ${polyWidth} ${polyHeight * 2} 0 ${polyHeight * 2}`;

    return polyLinePoints;

})



</script>