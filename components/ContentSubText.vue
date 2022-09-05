<template>
<p class="leading-loose text-xl">
  {{ content }}
</p>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const props = defineProps({
  text : {
    type: String,
    require: true
  }
})

const content = ref(props.text)
</script>
