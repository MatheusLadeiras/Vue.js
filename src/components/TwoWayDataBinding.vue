<template>
    <br><br><br>
    <div>
        ========================================<br>
        One-way data binding <br>
        Two-way data binding <br>
        v-model -> formulários
    </div>
    <br><br>
    <div>
        <label><strong>Nome</strong></label><br>
        <input v-model="name" type="text"><br>
        {{ name }}
    </div>
    <br><br>
    <div>
        <label><strong>Sports</strong></label><br>
        <select v-model="sports">
            <option value="">Escolha</option>
            <option value="Futebol">Futebol</option>
            <option value="Skate">Skate</option>
            <option value="Tenis">Tenis</option>
        </select><br>
        {{ sports }}
    </div>
    <br><br>
    <div>
        <label><strong>NewsLetter</strong></label><br>
        <input v-model="newsLetter" type="radio" value="Sim">Sim<br>
        <input v-model="newsLetter" type="radio" value="Não">Não<br>
        {{ newsLetter }}
    </div>
    <br><br>
    <div>
        <label><strong>Contrato</strong></label><br>
        <input v-model="contract" type="checkbox">Você aceita nossos termos?<br>
        {{ contract }}
    </div>
    <br><br>
    <div>
        <label><strong>Pesquisa</strong></label><br>
        <input v-model="colors" type="checkbox" value="Azul">Azul<br>
        <input v-model="colors" type="checkbox" value="Vermelho">Vermelho<br>
        <input v-model="colors" type="checkbox" value="Amarelo">Amarelo<br>
        {{ colors }}
    </div>

    
</template>

<script>
    export default {
    name: 'App',
    data() {
        return {
        name: 'Jon Snow',
        sports: 'Futebol',
        newsLetter: 'Sim',
        contract: 'false',
        colors: ['Azul','Vermelho','teste'],
        }
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
</style>