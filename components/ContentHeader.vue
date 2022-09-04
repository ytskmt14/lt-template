<template>
  <span class="text-2xl">{{ headerText }}</span>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const props = defineProps({
  text: {
    type: String,
    require: true
  }
})

const headerText = ref(props.text)
</script>
