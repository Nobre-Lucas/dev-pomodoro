<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <TaskContainer/>
  <HeaderContainer/>
  <StatisticsContainer/>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HeaderContainer from './components/HeaderContainer.vue';
import TaskContainer from './components/TaskContainer.vue';
import StatisticsContainer from './components/StatisticsContainer.vue';

export default defineComponent({
  name: 'App',
  components: {
    TaskContainer,
    HeaderContainer,
    StatisticsContainer
  }
});
</script>

<style>

</style>
