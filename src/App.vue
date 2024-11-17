<script setup>
import { onMounted, ref } from 'vue'
import axios from 'axios'

import Header from './components/Header.vue'
import Bunner from './components/Bunner.vue'
import Promotions from './components/Promotions.vue'

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
  <header>
    <Header />
  </header>
  <main>
    <Bunner />
    <Promotions :items="items" />
  </main>
</template>

<style scoped>
/* @media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
} */
</style>
