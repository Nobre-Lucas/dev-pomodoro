<template>
    <div class="wrapper">
        <TaskComponent />
        <StatisticsComponent />
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import TaskComponent from './TaskComponent.vue';
import StatisticsComponent from './StatisticsComponent.vue';

export default defineComponent ({
    name: 'ContentWrapper',
    components: {
    TaskComponent,
    StatisticsComponent
},
});
</script>

<style scoped>
.wrapper {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    position: absolute;
    height: auto;
    width: 100%;
    top: 1rem;
    bottom: 0;
}
</style>