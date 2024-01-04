<template>
    <br><br><br>
    <div>
        - Slots -<br>
        ========================================<br><br>
        <h1 v-if="$slots.title" class="title"><slot name="title" /></h1>
        <slot name="description"/>
        <slot/>
    </div>
</template>

<script>
    export default {
    mounted() {
        console.log(this.$slots.description);
    }, 
    name:'app',
    data() {
        return {
        }
    },

    computed: {
    },

    methods: {
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
