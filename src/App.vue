<script setup lang="ts">
import { useTemplateRef } from 'vue';
import Example from './components/Example.vue';

const exampleRef = useTemplateRef('example');
exampleRef.value?.$el.addEventListener('click', () => {});
//                ^ This fails because of the component Example.vue being generic
</script>

<template>
  <Example ref="example" />
</template>
