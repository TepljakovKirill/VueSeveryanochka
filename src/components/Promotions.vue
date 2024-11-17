<script setup>
import Card from './Card.vue'

defineProps({
  items: Array,
})
</script>
<template>
  <div class="container">
    <div class="section_title">
      <h2>Акции</h2>
      <a class="section_title-link" href="#">Все акции</a>
    </div>
    <div class="section_block flex">
      <Card
        v-for="item in items"
        :key="item.id"
        :imageUrl="item.imageUrl"
        :title="item.title"
        :priceDiscount="item.priceDiscount"
        :priceRegular="item.priceRegular"
      />
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
