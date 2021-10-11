<template>
  <h3>Meu nome é: {{ nome }}</h3>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: 'Ainda não sei',
        }
    },

    created() {
        this.nome = "Mateus";
    },

    mounted() {
        this.nome = "Henrique"
    }
}
</script>
