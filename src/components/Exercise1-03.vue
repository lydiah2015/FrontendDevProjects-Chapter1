<template>
<!-- <div> -->
    <!-- v-text="text"  -->
    <h1 v-once >
        
        <!-- {{ text }} -->
        Loading ...
    </h1>
    <h2 v-html="html" />

    
<!-- </div> -->
</template>
<script setup>
 const text ='Directive Text'

 const html =  'Stylise </br>HTML in <br/><b>your data</b>'
</script>
