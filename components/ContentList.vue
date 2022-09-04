<template>
  <ul>
    <li v-for="(listItem, index) in listItems" :key="index">
      {{ listItem }}
    </li>
  </ul>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const props = defineProps({
  items : {
    type: Array,
    require: true
  }
})

const listItems = ref(props.items)
</script>
