<script setup lang="ts">
import { computed, ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue'
import SlotsTest from './components/SlotsTest.vue'

const data = ref<string>('')
const capitalData = computed(():string=> data.value.toUpperCase())
</script>

<template>

  <SlotsTest>

    <template #header>
      <h3>Header line</h3>
      <HelloWorld v-model="data" />
      <h1>recive from child : <span>{{ capitalData }}</span></h1>
    </template>

    <template #footer>
      <h3>footer line</h3>
    </template>

  </SlotsTest>
  
</template>

