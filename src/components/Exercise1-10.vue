<script>
export default {
    data() {
        return {
            list: [
                'Apex Legends',
                'A Plague Tale: Innocence',
                'ART SQOOL',
                'Baba Is You',
                'Devil May Cry 5',
                'The Division 2',
                'Hypnospace Outlaw',
                'Katana ZERO',
                'testing unmouted hooks',
            ],
        }
    },
    beforeCreate() {
        alert('beforeCreate: data is static, thats it')
    },
    created() {
        alert('created: data and events ready, but no DOM')
    },
    methods: {
        deleteItem(value) {
            this.list = this.list.filter(item => item !== value)
        }

    },
    beforeUpdate() {
        alert('beforeUpdate: we know an update is about to happen, and have the data')
    },
    updated() {
        alert('updated: virtual DOM will update after you click OK')
    },
    beforeUnmount() {
        alert('beforeUnmount: about to blow up this component')
    },
    unmounted() {
        alert('unmounted: this component has been destroyed')
    },
}
</script>
<template>
    <div>
        <h1>Vue LifeCycle Hooks</h1>
        <ul>
            <li v-for="(item, n) in list" :key="n">
                {{ item }}
                <button @click="deleteItem(item)">DELETE ITEM</button>
            </li>
        </ul>
    </div>
</template>
<!-- <style lang="stylus">
ul
  color:#2c3e50;
    > h2
    color:#22cc33;

</style> -->