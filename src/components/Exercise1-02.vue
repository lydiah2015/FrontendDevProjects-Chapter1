<!-- composition api -->

<!-- <template>
<div>
    <h1>
        {{ title.toUpperCase() }}
    </h1>
</div>
</template>
<script setup>
const title = 'My first component'

</script> -->
<!-- <style>
</style> -->


<!-- options api -->
<template>
<h1>
    {{ isUppercase ? title.toUpperCase() : title}}
</h1>
</template>
<script>
export default {
    data() {
        return {
            title:'My first Component',
            isUppercase :true
        }
    }
}
</script>