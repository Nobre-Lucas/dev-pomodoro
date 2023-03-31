<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <header>
    <HeaderContainer/>
  </header>
  <body>
    <div class="wrapper">
      <TaskContainer/>
      <StatisticsContainer/>
    </div>
  </body>
  <footer>
      <FooterContainer/>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HeaderContainer from './components/HeaderContainer.vue';
import TaskContainer from './components/TaskContainer.vue';
import StatisticsContainer from './components/StatisticsContainer.vue';
import FooterContainer from './components/FooterContainer.vue';

export default defineComponent({
  name: 'App',
  components: {
    TaskContainer,
    HeaderContainer,
    StatisticsContainer,
    FooterContainer
  }
});
</script>

<style>

  .wrapper {
    display: grid;
    grid-template-columns: 50% 50%;
    grid-template-rows: 100%;
  }

  .statistics {
    grid-column: auto;
    grid-row: auto;
  }

  .task {
    grid-column: auto;
    grid-row: auto;
  }

</style>
