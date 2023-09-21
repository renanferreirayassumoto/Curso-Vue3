<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou procurando uma vaga de emprego.</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
            <li>Java</li>
            <li>WordPress</li>
            <li>vue</li>
            <li>C</li>
        </ul>
        <div>
            <button @click="showEmail"> {{ textoBotao }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p class="teste">Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue';

export default {
    name: 'Info',
    components: {
        Picture,
    },
    data() {
        return {
            esta_trabalhando: false,
            mostrar_email: false,
            email: 'renan@gmail.com',
            meu_link: 'https:www.google.com.br',
            textoBotao: 'Mostrar e-mail'
        }
    },
    methods: {
        showEmail() {
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email){
                this.textoBotao = "Mostrar e-mail"
            }else{
                this.textoBotao = "Esconder e-mail"
            }
        }
    }
}
</script>