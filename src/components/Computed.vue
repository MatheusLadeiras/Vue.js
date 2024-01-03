<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <br><br><br>
    <div>
        - Conputed -<br>
        ========================================<br><br>
        {{ user.first_name }} {{ user.last_name }}
        {{ fullName }}
        
    </div>
</template>

<script>
    export default {
    name:'app',
    data() {
        return {
            user: {
                first_Name: 'Jon',
                last_Name: 'Snow',
            }
        }
    },

    computed: {
        fullName () {
            return `${this.user.first_Name} ${this.user.last_Name}`
        },
    },

    methods: {
        click() {
            console.log(this.user);
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
