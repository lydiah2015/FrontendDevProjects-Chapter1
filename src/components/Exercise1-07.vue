<script setup>
const information = {
    title: "My list component information",
    subtitle: "Vue JS basics",
    items: ["Looping", "Data", "Methods"],
}
</script>
<template>
    <div class="objs">
        <h1>
            Looping through Objects
        </h1>
        <ol v-for="(value, key) in information" :key="key">
            {{ key }} : {{ value.toString() }}
    </ol>
    </div>
</template>
<style>
.objs{
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    
}</style>