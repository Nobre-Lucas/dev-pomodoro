<template>
  <HeaderComponent />
  <ContentWrapper />
  <FooterComponent />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import ContentWrapper from './components/ContentWrapper.vue';

export default defineComponent({
  name: 'App',
  components: {
    HeaderComponent,
    FooterComponent,
    ContentWrapper,
  }
});
</script>

<style></style>
