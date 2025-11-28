<script setup>
    console.log("Hello Vue Component");

    const hello = "<b>Belajar template</b>";
    const vHtml = "<h1>Belajar template (dipanggil sebagai html dengan directive html v-)</h1>";
</script>

<template>
    <h1 class="hello">Hello Vue Component</h1>
    <h1 class="hello">{{hello}} (dipanggil dengan mustache, dirender sebagai string)</h1>
    <div v-html="vHtml"></div>
</template>

<style scoped>

.hello{
    color: green;
}

</style>