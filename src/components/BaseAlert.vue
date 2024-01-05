<template>
    <br><br><br>
    <div>
        - Base Alert -<br>
        ========================================<br><br>
        <div :class="['alert', {'alert-success': variant === 'success'}]">Seu formulário foi enviado com sucesso</div><br>
    </div>
</template>

<script>
    export default {
        props: ['variant'],
    }
</script>


<style scoped>
    .alert {
        padding: 17px;
        border-radius: 10px;
        color: rgb(255, 230, 0);
        background: red;
    }
    .alert-success {
        background: rgb(72, 255, 0);
        color: #fff;
    }
</style>
