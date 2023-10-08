<template>
    <div class="arrs">
        <h1>Working with vue directive V-FOR and V-IF</h1>
        <ul class="lists">
            <li v-for="(interest, index) in interests" :key="index">
                {{ interest.title }}
                <ol v-if="interest.favorites.length >0">

            <li v-for="(fav, m) in interest.favorites" :key="m">
                {{ fav }}
            </li>
            </ol>
            </li>
           
        </ul>
    </div>
</template>
<script setup>
const interests = [
    {
        title: "TV",
        favorites: ["Designated Survivor", "Spongebob"],
    },
    {
        title: "Games",
        favorites: ["CS:GO"],
    },
    {
        title: "Sports",
        favorites: [],
    },
];
</script>
<style>
.arr {
    display: flex;
    justify-content: space-around;
    flex-direction: column;

}

.lists {
    color: orangered;
}
</style>