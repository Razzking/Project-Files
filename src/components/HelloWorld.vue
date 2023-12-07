<template>

  <h1> recive from parent :  <span>{{ modelValue }}</span></h1>
  <input type="text" :value="modelValue" @input="$emit('update:modelValue',$event.target.value)">

</template>

<script setup lang="ts">

defineProps({
  modelValue:{
    type:String
  }
})

defineEmits(['update:modelValue'])

</script>

<style>
span{
  color: crimson;
}
</style>