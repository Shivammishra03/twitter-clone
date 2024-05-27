<script lang="ts" setup>
import MainSection from '../components/MainSection.vue';

const loading = ref(false);


</script>

<template>
  <div>
    <MainSection title="Home" :loading="loading">
      content type
    </MainSection>
  </div>
</template>
