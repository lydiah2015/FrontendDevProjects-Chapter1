<template>
    <div class="form">
        <label class="label">
            Name
        </label>
        <input class="input-box" type="text" v-model="name" />
        <label class="label">
            Preffered Javascript style
        </label>
        <select class="input-box" name="language" v-model="language">
            <option value="Javascript">
                JavaScript
            </option>
            <option value="TypeScript">
                TypeScript
            </option>
            <option value="CoffeeScript">
                CoffeeScript
            </option>
            <option value="Dart">
                Dart
            </option>
        </select>

        <ul class="overview">
            <li><strong>Overview</strong></li>
            <li>Name:{{ name }}</li>
            <li>Preference:{{ language }}</li>
        </ul>
    </div>
</template>
<script>
export default {
    data() {
        return {
            name: '',
            language: ''
        }
    },
}
</script>
<style>
.form {
    display: flex;
    justify-content: space-evenly;
    max-width:1000px;
    padding: 40px 20px;
    border-radius: 10px;
    margin: 0 auto;
    background: #ececec;
}

.overview {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    max-width: 800px;
    margin: 40px auto;
    padding: 40px 20px;
    border-radius: 10px;
    border: 1px solid #ececec;
    color:blue;
}

.overview>li {
    list-style: none;
}

.overview>li+li {
    margin-top: 20px;
}
.label{
color: black;
/* width:75%; */
margin-right: 15px;
margin-left: 15px;
font-size: 15px;

}

.input-box{
width:180px;
height:30px;
}
</style>