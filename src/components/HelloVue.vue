<script setup>
    console.log("Hello Vue Component");

    const hello = "<b>Belajar template</b>";
    const vHtml = "<h1>Belajar template (dipanggil sebagai html dengan directive html v-)</h1>";

    /* Directive class | v-bind:class, :class, :id */
    const classHello = "hello";
    const id = "id-name";
</script>

<template>
    <h1 class="hello">Hello Vue Component</h1>
    <h1 class="hello">{{hello}} (dipanggil dengan mustache, dirender sebagai string)</h1>
    <div v-html="vHtml"></div>

    
    <h1 :id v-bind:class="classHello">Memanggil class dengan directive class v-bind:class</h1>
    <div :class="classHello" v-html="hello"></div>
</template>

<style scoped>

.hello{
    color: green;
}

</style>