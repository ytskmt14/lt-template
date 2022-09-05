<template>
<p class="leading-loose text-3xl">
  <a class="underline text-blue-700" :href="url">
    {{ content }}
  </a>
</p>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const props = defineProps({
  text : {
    type: String,
    require: true,
  },
  url : {
    type: String,
    require: true,
  }
})

const content = ref(props.text)
const url = ref(props.url)
</script>
