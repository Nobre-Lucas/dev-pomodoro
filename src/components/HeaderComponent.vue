<template>
    <header>
        <h2>Cabeçalho</h2>
    </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'HeaderContainer'
})
</script>

<style scoped>
header {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: brown;
}
</style>