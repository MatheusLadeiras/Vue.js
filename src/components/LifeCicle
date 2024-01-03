<template>
    <br><br><br>
    <div>
        - Life Cicle -<br>
        ========================================<br><br>
        <h1 v-if="showHeader">{{ name }}</h1> <br>
        <button @click="showHeader = !showHeader">
            Toggle
        </button><br><br>
        <input v-model="name" type="text">
    </div>
</template>

<script>
    export default {
    name:'app',
    data() {
        return {
            name: 'Jon Snow',
            showHeader: true,
        }
    },

    //HOOKS
    beforeCreate() {
        console.log('beforeCreate');
        console.log('Estado:', this.name);
        console.log('DOM',this.$el);
    },
    created() {
        console.log('Created');
        console.log('Estado:', this.name);
        console.log('DOM',this.$el);
    },
    beforeMount() {
        console.log('beforeMount');
        console.log('Estado:', this.name);
        console.log('DOM',this.$el);
    },
    mounted() {
        console.log('mounted');
        console.log('Estado:', this.name);
        console.log('DOM',this.$el);
        window.removeEventListener('resize', resize)
    },
    beforeUnmount() {
        console.log('beforeUnmount');
        console.log('Estado:', this.name);
        console.log('DOM',this.$el);
    },
    unmounted() {
        console.log('Unmounted');
        console.log('Estado:', this.name);
        console.log('DOM',this.$el);
    },
    beforeUpdate() {
        console.log('beforeUpdate:', this.name);
    },
    uptated() {
        console.log('uptated:', this.name);
    },

    watch: {
    },

    computed: {
    },

    methods: {
        resize($evt) {
            console.log($evt);
        }
    },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
