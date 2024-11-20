<script setup>
const menuItems = [
  { id: 1, name: 'О комании', link: '#' },
  { id: 2, name: 'Контакты', link: '/#' },
  { id: 3, name: 'Вакансии', link: '/#' },
  { id: 4, name: 'Статьи', link: '/#' },
  { id: 5, name: 'Политика обработки персональных данных', link: '/#' },
]
</script>

<template>
  <div class="footer">
    <div class="container">
      <div class="footer_contaner flex">
        <div class="footer_container-left flex">
          <RouterLink to="/">
            <img src="/logo-footer.svg" alt="Логотип" />
          </RouterLink>
          <ul class="footer_menu flex">
            <li class="footer_menu-list" v-for="item in menuItems" :key="item.id">
              <router-link class="footer_menu-link" :to="item.link">
                {{ item.name }}
              </router-link>
            </li>
          </ul>
        </div>
        <div class="footer_container-right grid">
          <div class="footer_socal-block grid">
            <a class="socal-block" href="#"
              ><img class="footer_socal-img" src="/instagram.png" alt="инстаграмм"
            /></a>
            <a class="socal-block" href="#"
              ><img class="footer_socal-img" src="/vk.svg" alt="в контакте"
            /></a>
            <a class="socal-block" href="#"
              ><img class="footer_socal-img" src="/facebook.png" alt="фейсбук"
            /></a>
            <a class="socal-block" href="#"
              ><img class="footer_socal-img" src="/odnoklassnyki.svg" alt="одноклассники"
            /></a>
          </div>
          <a class="footer_phone" href="tel:+7 800 777 33 33">8 800 777 33 33</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.footer {
  width: 100%;
  background: url(/bg-footer.png);
  background-repeat: no-repeat;
  background-position: center;
}

.footer_contaner {
  height: 126px;
  align-items: center;
  justify-content: space-between;
  align-items: center;
}

.footer_container-left {
  align-items: center;
}

.footer_menu {
  flex-wrap: wrap;
  list-style: none;
}

.footer_menu-list:not(:last-child) {
  margin-right: 38px;
}

.footer_menu-link {
  font-size: 12px;
  font-family: 'Rubik';
  color: #414141;
}

.footer_container-right {
  grid-template-columns: 1fr;
  grid-template-rows: repeat(2, 1fr);
  grid-column-gap: 17px;
  grid-row-gap: 17px;
}

.footer_socal-block {
  grid-template-columns: repeat(4, 1fr);
  gap: 17px;
}

.footer_socal-img {
  object-fit: cover;
}

.footer_phone {
  width: 158px;
  background: url(/phone.svg);
  padding-left: 37px;
  background-position: 8px 0px;
  background-repeat: no-repeat;
  font-size: 16px;
  color: #414141;
}

@media (max-width: 1115px) {
}
</style>
