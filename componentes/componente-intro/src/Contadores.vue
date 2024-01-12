<template>
    <div class="contadores">
        <h1>Contadores</h1>
        <app-contador v-for="c in 5" :key="c" />
    </div>
</template>

<script>
import contador from './Contador.vue';
export default {
    components: { 'app-contador': contador },
};
</script>

<style></style>
