<template>
    <div>
        <p>Primeiro componente</p>
        <p>Meu nome é {{ nome }}</p>
    </div>
</template>

<script>
    export default {
        name: 'PrimeiroComponente',
        data() {
            return {
                nome: 'Mateus'
            }
        }
    }
</script>