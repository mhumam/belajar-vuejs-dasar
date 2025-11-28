<script setup>
    console.log("Hello Vue Component");

    const hello = "<b>Belajar template</b>";
    const vHtml = "<h1>Belajar template (dipanggil sebagai html dengan directive html v-)</h1>";

    /* Directive class | v-bind:class, :class, :id */
    const classHello = "hello";
    const id = "id-name";

    const buttonDisabled = true;
    const buttonEnabled = false;

    const helloMultipleAttributed = "<h1>Belajar template multiple attributes</h1>";
    const dataMultipleAttribute = {
        id: "hello",
        class: "hello"
    };

    const helloFunction = () => {
        return "Hello Function";
    }

</script>

<template>
    <h1 class="hello">Hello Vue Component</h1>
    <h1 class="hello">{{ hello }} (dipanggil dengan mustache, dirender sebagai string)</h1>
    <div v-html="vHtml"></div>
    
    <h1 :id v-bind:class="classHello">Memanggil class dengan directive class v-bind:class</h1>
    <div :class="classHello" v-html="hello"></div>

    <button :disabled="buttonDisabled">Button disabled</button>
    <button :disabled="buttonEnabled">Button enabled</button>

    <h1 v-bind="dataMultipleAttribute">{{ helloMultipleAttributed }}</h1>
    <div :class="dataMultipleAttribute.class" v-html="helloMultipleAttributed"></div>
    
    <h1 v-bind="dataMultipleAttribute">{{ "JS Expression".toUpperCase() }}</h1>
    <h2>{{ helloFunction() }}</h2>
    <h2>{{ 500 * 100 }}</h2>
</template>

<style scoped>

.hello{
    color: green;
}

</style>