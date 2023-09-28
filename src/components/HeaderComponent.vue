<template>
    <header>
        <nav class="navbar" role="navigation" aria-label="main navigation">
            <div class="navbar-brand">
                <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false"
                    data-target="pomodoroNavBar">
                    <span aria-hidden="true"></span>
                    <span aria-hidden="true"></span>
                    <span aria-hidden="true"></span>
                </a>
            </div>

            <div id="pomodoroNavBar" class="navbar-menu">
                <div class="navbar-start">
                    <a class="navbar-item">
                        About
                    </a>

                    <a class="navbar-item">
                        Contact
                    </a>
                </div>

                <div class="navbar-end">
                    <div class="navbar-item">
                        <div class="buttons">
                            <a class="button is-primary">
                                <strong>Sign up</strong>
                            </a>
                            <a class="button is-light">
                                Log in
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </nav>
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
    /* background-color: brown; */
}
</style>