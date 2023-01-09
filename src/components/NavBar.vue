
<template>
    <nav>
        <div class="title">
            <h4>{{title}}</h4>
        </div>

        <a href="http://www.google.es" target="_blank">Google</a>
        <a href="http://www.vuejs.org" target="_blank">Vue</a>
    </nav>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent ({
    name: "NavBar",
    props: {
        title: {
            type: String,
            required: true
        }
    }
});
</script>

<style scoped>
    a {
        color: red;
    }

    nav {
        width: 90%;
        display: flex;
        justify-content: space-between;
        padding: 30px;
        background-color: #2c3e50;
        color:white;
    }
</style>