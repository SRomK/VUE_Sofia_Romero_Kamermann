
<template>
    <nav>
        <div class="title">
            <h4>{{title}}</h4>
        </div>



        <a href="http://www.google.es" target="_blank">Google</a>
        <a href="http://www.vuejs.org" target="_blank">Vue</a>
    
        <div class="subtitle">
            <h6>{{subtitle}}</h6>
        </div>
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
        },
        subtitle: {
            type: String,
            required: true
        },
        links: {
            type: Array,
            default() {
                return [
                {label: 'Google', link: 'http://www.google.es'},
                {label: 'vue', link: 'http://www.vuejs.org'}

                ];
            },
        },
    },
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

    .subtitle {
        color:aquamarine;
        width: 50px;
    }


</style>