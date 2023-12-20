<template>
    <div>
        <h1 :class="{ 'title': true, 'title-home': isHome}">
            Curso Vue 3
        </h1>
        <p :class="pClass">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
        </p>
        <p :style="{ 'color': 'aqua', 'background-color': 'black' }">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
        </p>
        <div v-for="(obj, index) in todos" :key="obj.id" class="todos-item">
            <img v-if="obj.imgSrc" :alt="obj.imgSrc">
            {{ index+1 }} - {{ obj.title }}
        </div>
    </div> 
</template>

<script>
    export default {
        name: 'App',
        data() {
            return {
                isHome: true,
                classVar:'title',
                pClass: ['text', 'text-home'],
                todos: [
                            {
                                "userId": 10,
                                "id": 197,
                                "title": "dignissimos quo nobis earum saepe",
                                "completed": true,
                                "imgSrc": 'https://placehold.co/150x150',
                            },
                            {
                                "userId": 10,
                                "id": 198,
                                "title": "quis eius est sint explicabo",
                                "completed": true,
                                "imgSrc": 'https://placehold.co/150x150',
                            },
                            {
                                "userId": 10,
                                "id": 199,
                                "title": "numquam repellendus a magnam",
                                "completed": true,
                                "imgSrc": 'https://placehold.co/150x150',
                            },
                            {
                                "userId": 10,
                                "id": 200,
                                "title": "ipsam aperiam voluptates qui",
                                "completed": false,
                                //"imgSrc": 'https://placehold.co/150x150',
                            },
                        ]
            }
        }
    }
</script>

<style>
    .title{
        font-size: 20px;
        color: blue;
    }
    .title-home{
        font-size: 40px;
        color: green;
    }
    .text {
        color: yellow;
    }
    .text-home {
        color: rgb(255, 38, 0);
    }
    .todos-item {
        background: #000;
        margin: 0 0 5px 0;
        padding : 3px 6px;
        color: #fff;
    }
    .header {
        background: black;
        color: #fff;
    }
    #app {
        font-family: Arial, Helvetica, sans-serif;
        color: #2c3e50;
        margin: 600px;
    }
</style>