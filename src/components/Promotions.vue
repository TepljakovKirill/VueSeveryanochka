<script setup>
import Card from './Card.vue'
</script>
<template>
  <div class="container">
    <div class="section_title">
      <h2>Акции</h2>
      <a class="section_title-link" href="#">Все акции</a>
    </div>
    <div class="section_block flex">
      <Card />
      <Card />
      <Card />
      <Card />
    </div>
  </div>
</template>

<style scoped>
.section_title {
  margin-top: 30px;
  margin-bottom: 40px;
}

.section_block {
  margin-bottom: 40px;
  justify-content: space-between;
}
</style>
