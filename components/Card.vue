<template>
    <div v-bind:class="classes.cont">{{ data.name }}</div>
    <Handle id="a" type="source" :position="Position.Right" :class="classes.source" />
    <!-- <Handle id="b" type="target" :position="Position.Left" :class="classes.target" /> -->
</template>


<script setup>
import { Handle, Position } from "@vue-flow/core";
const props = defineProps(["data"])

</script>


<style module="classes">

.cont {
    width: 145px;
    color: brown;
    text-align: center;
    padding: 20px 0px;
    border: 2px solid black;
}

.source {
    background-color: red;
    filter: invert(100%);
}

.target {
    background-color: black;
    filter: invert(100%);
}


</style>