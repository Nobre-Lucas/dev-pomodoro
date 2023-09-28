<template>
    <footer class="footer">
        <div class="content has-text-centered">
            <p>
                <strong>PomodoroDev</strong> by <a href="https://nobre-lucas.github.io/portfolio/" target="_blank">Lucas Nobre Barbosa</a>
            </p>
        </div>
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
}
</style>