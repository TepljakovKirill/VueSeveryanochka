<script setup>
import Card from './Card.vue'

defineProps({
  items: Array,
})
</script>
<template>
  <div class="container">
    <div class="section_title">
      <h2 class="section_title-block">Акции</h2>
      <a class="section_title-link" href="#">Все акции</a>
    </div>
    <div class="section_block grid">
      <Card
        v-for="item in items"
        :key="item.id"
        :imageUrl="item.imageUrl"
        :title="item.title"
        :priceDiscount="item.priceDiscount"
        :priceRegular="item.priceRegular"
        :stars="item.stars"
      />
    </div>
  </div>
</template>

<style scoped>
.section_title-block {
  font-size: 36px;
}
.section_title {
  margin-top: 30px;
  margin-bottom: 40px;
}

.section_block {
  grid-gap: 20px;
  grid-template-columns: repeat(auto-fill, 272px);
  justify-content: space-between;
}

@media (max-width: 768px) {
  .section_title-block {
    font-size: 24px;
  }

  .section_block {
    grid-gap: 10px;
  }
}

@media (max-width: 574px) {
  .section_block {
    grid-template-columns: repeat(2, 224px);
  }
}

@media (max-width: 478px) {
  .section_block {
    grid-template-columns: repeat(2, 160px);
  }
}
</style>
