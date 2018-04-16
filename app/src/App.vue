<template>
    <div id="app">
        <img src="./assets/logo.png">
        <inline-tags-input v-model="tags" />
    </div>
</template>

<script>
import InlineTagsInput from "./components/inline-tags-input";

export default {
    name: "App",
    components: {
        InlineTagsInput
    },
    data() {
        return {
            tags: []
        };
    }
};
</script>

<style>
#app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
