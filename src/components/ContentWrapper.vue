<template>
    <div class="content columns">
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

.content {
    padding-top: 4rem;
    height: 100%;
    width: 100%;
}

</style>