<template>
  <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades.</p>

        <p>Utilizo as seguintes tecnologias para Backend:</p>
        <ul>
            <li v-for="(technology, index) in backend_technologies" :key="index">{{ technology }}</li>
        </ul>

        <p>Utilizo as seguintes tecnologias para Frontend:</p>
        <ul>
            <li v-for="(technology) in frontend" :key="technology.id">
                {{ technology.language }}
            </li>
        </ul>
        <div>
            <button @click="mostrarEmail">Mostrar e-mail</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
  </div>
</template>

<script>
export default {
    name: 'Info',

    data() {
        return {
            esta_trabalhando: false,
            mostrar_email: false,
            email: 'email@email.com',
            meu_link: 'https://www.google.com',
            backend_technologies: [
                "Javascript",
                "Php",
                "Python",
            ],
            frontend: [
                {id: 1, language: "HTML"},
                {id: 2, language: "CSS"},
                {id: 3, language: "Vue.js"},
            ]
        }
    },

    methods: {
        mostrarEmail() {
            this.mostrar_email = !this.mostrar_email
        }
    },
}
</script>
