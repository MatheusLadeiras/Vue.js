<template>
    <br><br><br>
    <div>
        - Observers -<br>
        ========================================<br><br>
        <input v-model="name" type="text"> <br>
        {{ name }}<br>

        <input v-model="user.first_name" type="text"> <br>
        <input v-model="user.last_name" type="text"> <br>
        {{ user.first_name }} 
        {{ user.last_name }} <br>

        <select v-model="pageCount">
            <option value="5">5</option>
            <option value="10">10</option>
            <option value="15">15</option>
        </select> <br>
        {{ pageCount }}
    </div>
</template>

<script>
    export default {
    name:'app',
    data() {
        return {
            name: '',
            pageCount: 5,
            user: {
                first_name: '',
                last_name: '',
            }
        }
    },

    watch: {
        name() {
            this.saveUserName()
        },
        pageCount() {
            this.changePage();
        },
        user: {
            handler() {
                console.log('User alterado');
            },
            deep: true,//A observação é profunda se baseando no handler, se fosse função a alteração não iria funcionar, mais na aula 11
        },
    },

    computed: {
    },

    methods: {
        saveUserName() {
            console.log('ajax');
            console.log(this.name);
        },
        changePage() {
            console.log('Ajax changePage')
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
