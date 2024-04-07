<template>
    <div class="card">
        <h3>{{ data.title }}</h3>
        <br>
        <h2>{{ data.price }}</h2>
        <span>{{ data.time }}</span>
        <br>
        <br>
        <ul>
            <li v-for="element, index in data.features" :key="index">{{ element }}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: ['data']
    }
</script>

<style scoped>
    .card {
    border: 2px solid rgb(229, 229, 229);
    border-radius: 6px;
    padding: 32px 24px;
    line-height: 1.5;
    color: rgb(0, 0, 0);
    position: relative;
}
ul {
    list-style: url(/static/icons8-галочка-50.png);
    margin: 0px;
    padding: 0px;
    text-align: left;
}
li {
    margin-bottom: 4px;
    padding-left: 22px;
    color: rgb(0, 0, 0);
    font-weight: 350;
    display: flex;
    align-items: baseline;
    gap: 6px;
}
</style>