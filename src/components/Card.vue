<script setup>
import { ref } from 'vue'

defineProps({
  imageUrl: String,
  title: String,
  priceDiscount: String,
  priceRegular: String,
  stars: Number,
})

const isLiked = ref(false)
const onClickFavorite = () => {
  isLiked.value = !isLiked.value
}
</script>

<template>
  <div class="card">
    <div class="card_img-block">
      <img class="card_img" :src="imageUrl" alt="Товар" />
      <div @click="onClickFavorite" class="card_img-favorite flex">
        <img :src="isLiked ? '/favoriteOn.svg' : '/favorite.svg'" alt="Избранное" />
      </div>
      <p class="card_img-discount flex">-50%</p>
    </div>

    <div class="card_content">
      <div class="card_price flex">
        <div class="card_price-block">
          <p class="card_price-discount">{{ priceDiscount }} ₽</p>
          <p class="card_price-card">С картой</p>
        </div>

        <div class="card_price-block">
          <p class="card_price-regular">{{ priceRegular }} ₽</p>
          <p class="card_price-card">Обычная</p>
        </div>
      </div>
      <p class="card_title">{{ title }}</p>
      <div class="card_star-wrap">
        <div class="card_star-block">
          <span v-for="star in 5" :key="star">
            <img src="/star.svg" alt="Звезда" />
          </span>
          <div class="card_star-block">
            <span v-for="star in stars" :key="star">
              <img src="/star-red.svg" alt="Звезда" />
            </span>
          </div>
        </div>
      </div>

      <button class="card-button">В корзину</button>
    </div>
  </div>
</template>

<style scoped>
.card {
  width: 272px;
  box-shadow: 1px 2px 4px 0px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  background-color: white;
}

.card_img-block {
  position: relative;
}

.card_img-favorite {
  position: absolute;
  top: 8px;
  right: 8px;
  width: 32px;
  height: 32px;
  border-radius: 4px;
  background-color: rgb(243, 242, 241);
  justify-content: center;
  align-items: center;
  object-fit: cover;
  cursor: pointer;
}

.card_img-discount {
  position: absolute;
  left: 10px;
  bottom: 10px;
  width: 56px;
  height: 32px;
  justify-content: center;
  align-items: center;
  color: white;
  border-radius: 4px;
  background-color: rgb(255, 102, 51);
}

.card_img {
  padding-top: 3px;
}

.card_content {
  padding: 8px;
}

.card_price {
  justify-content: space-between;
  margin-bottom: 8px;
}

.card_price-block:not(:first-child) {
  text-align: right;
}

.card_price-discount {
  font-size: 18px;
  font-weight: 700;
}

.card_price-regular {
  font-size: 16px;
  color: #606060;
}

.card_price-card {
  margin-top: 5px;
  font-size: 12px;
  color: #bfbfbf;
}

.card_title {
  margin-top: 10px;
  margin-bottom: 10px;
}

.card-button {
  width: 100%;
  height: 40px;
  font-size: 16px;
  color: rgb(112, 192, 91);
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid rgb(112, 192, 91);
  border-radius: 4px;
  background-color: transparent;
  cursor: pointer;
  transition: 0.3s ease-in;
}

.card-button:hover {
  color: white;
  border: 1px solid transparent;
  border-radius: 4px;
  background-color: rgb(255, 102, 51);
  border: 1px solid rgb(255, 102, 51);
  transition: 0.3s ease-in;
}

.card_star-wrap {
  position: relative;
  padding: 10px 0;
}

.card_star-block {
  display: inline-flex;
  height: 16px;
  position: absolute;
  top: 0;
  left: 0;
}

@media (max-width: 574px) {
  .card {
    width: 224px;
  }
}

@media (max-width: 478px) {
  .card {
    width: 160px;
  }
}
</style>
