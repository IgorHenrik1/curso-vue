<template>
    <div class="container">
        <h1>Componente Usuário</h1>
        <p>Esse é um componente muito legal!</p>
        <p>Nome é <strong>{{ nome }}</strong></p>
        <p>Idade é <strong>{{ idade }}</strong></p>
        <button @click="alterarNome">
            Alterar Nome
        </button>
        <hr>
        <div class="componentes">
            <app-usuario-info :nome="nome" @nomeMudou="nome = $event" :reniciarFN="reniciarNome" :idade="idade"/>
            <app-usuario-editar :idade="idade" />
        </div>
    </div>
</template>

<script>
import AppUsuarioEditar from './UsuarioEditar';
import AppUsuarioInfo from './UsuarioInfo';

export default {
    components: { AppUsuarioInfo, AppUsuarioEditar },
    data() {
        return {
            nome: 'Pedro',
            idade: 21,
        };
    },
    methods: {
        alterarNome() {
            if (this.nome == 'Pedro') {
                this.nome = 'Ana';
            } else {
                this.nome = 'Pedro';
            }
        },

        reniciarNome() {
            this.nome = 'Pedro';
        },
    },
};
</script>

<style scoped>
.container {
    background-color: #27363b;
    color: #fff;
    padding: 10px;
}

.container hr {
    margin: 20px 10px;
}

.componentes {
    display: flex;
}

.componentes > * {
    margin: 10px;
}
</style>
