<script setup>
const hoverMenuItems = [
  { id: 1, name: 'Молоко, сыр, яйцо', link: '/#' },
  { id: 2, name: 'Хлеб', link: '/#' },
  { id: 3, name: 'Овощи и фрукты', link: '/#' },
  { id: 4, name: 'Замороженные продукты', link: '/#' },
  { id: 5, name: 'Напитки', link: '/#' },
  { id: 6, name: 'Чай, кофе', link: '/#' },
  { id: 7, name: 'Бакалея', link: '/#' },
  { id: 8, name: 'Здоровое итание', link: '/#' },
  { id: 9, name: 'Зоотоавры', link: '/#' },
  { id: 10, name: 'Детские товары', link: '/#' },
  { id: 11, name: 'Мясо, птица, колбаса', link: '/#' },
  { id: 12, name: 'Непродовольственные товары', link: '/#' },
]
</script>
<template>
  <div class="hover_catalog">
    <div class="hover_catalog-wrap">
      <ul class="hover_catalog-list grid">
        <li v-for="item in hoverMenuItems" :key="item.id">
          <router-link class="hover_catalog-link" :to="item.link">
            {{ item.name }}
          </router-link>
        </li>
      </ul>
    </div>
  </div>
</template>
<style scoped>
.hover_catalog {
  width: 100%;
  background-color: white;
  position: absolute;
  top: 72px;
  left: 0;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.15);
  z-index: 100;
}

.hover_catalog-wrap {
  max-width: 1208px;
  margin: 0 auto;
  padding: 0 10px;
}

.hover_catalog-list {
  padding: 40px 0;
  grid-template-columns: auto auto auto auto;
  grid-auto-flow: row;
  gap: 24px;
}

.hover_catalog-link {
  font-size: 16px;
  font-weight: 700;
  color: #414141;
  transition: 0.3s ease-in;
}

.hover_catalog-link:hover {
  color: rgb(255, 102, 51);
  transition: 0.3s ease-in;
}

@media (max-width: 768px) {
  .hover_catalog-list {
    padding: 40px 0;
    grid-template-columns: auto auto;
    grid-auto-flow: row;
    gap: 24px;
  }
}

@media (max-width: 360px) {
  .hover_catalog {
    display: none;
  }
}
</style>
