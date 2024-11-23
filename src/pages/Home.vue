<script setup>
import { onMounted, ref } from 'vue'
import axios from 'axios'

import Bunner from '../components/Bunner.vue'
import Promotions from '../components/Promotions.vue'

const items = ref([])

onMounted(async () => {
  try {
    const { data } = await axios.get('https://3c5a1e6c8b632c9f.mokky.dev/items')
    items.value = data
  } catch (err) {
    console.log(err)
  }
})
</script>

<template>
  <Bunner />
  <Promotions :items="items" />
</template>

<style scoped></style>
