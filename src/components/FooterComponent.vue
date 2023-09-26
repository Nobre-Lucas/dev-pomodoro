<template>
    <footer>
        <h2>Footer</h2>
    </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'FooterContainer'
})
</script>

<style scoped>
footer {
    position: fixed;
    bottom: 0;
    width: 100%;
    background-color: brown;
}
</style>