<template>
    <div id="app">
        {{ titulo }}
        <button @click="titulo += '#'">Alterar</button>
    </div>
</template>

<script>
export default {
    data: function () {
        return {
            titulo: 'Teste Data usando VueJS',
        };
    },
};
</script>

<style>
#app {
    background-color: blue;
    color: #fff;
}
</style>
