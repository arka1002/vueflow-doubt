<template>
    <div v-bind:class="classes.cont">{{ data.name }}</div>
</template>


<script setup>

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

</style>