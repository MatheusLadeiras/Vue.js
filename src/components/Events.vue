<template>
    <br><br><br>
    <div>
        ========================================<br><br>
        <button @click="onClick">
            Enviar
        </button>
    </div>
    <br><br>
    <div class="background"
         @mouseover="onMouseOver"
         @mouseout="onMouseOut"> Mouse over
    </div>
    <br><br>
    <form action="https://google.com/" @submit="onSubmit">
        <input type="text" @keyup="onKeyUp">
        <button type="submit">
            Submit
        </button>
    </form>
</template>

<script>
    export default {
    name: 'App',
    data() {
        return {
        }
    },

    methods: {
        onClick($evt) {
            console.log('click', $evt);
        },
        onMouseOver($evt) {
            console.log('mouse over', $evt);
        },
        onMouseOut($evt) {
            console.log('mouse out', $evt);
        },
        onSubmit($evt) {
            console.log('Submited', $evt);
        },
        onKeyUp($evt) {
            console.log('onKeyUp', $evt);
        },
    }
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

.background{
    padding: 10px;
    background-color: black;
    border-radius: 100px;
    color: white;
    margin: 0px 120px;
}
</style>