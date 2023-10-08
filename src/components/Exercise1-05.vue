<template>
    <div class="arrays">
    <h1>Looping through Arrays</h1>
    <ul>
        <li v-for="(interest, index) in interests" :key="index">
            {{ interest }}
        </li>
    </ul>
    </div>
</template>
<script setup>
const interests = ["Painting", "StarGazing", "Swimming", "Football"]
</script>
<style>
.arrays{
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: crimson;
}
</style>