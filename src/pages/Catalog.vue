<script setup></script>

<template>
  <div class="catalog">
    <div class="container">
      <div class="catalog_wrap">
        <p class="catalog_title">Каталог</p>
        <div class="catalog_menu flex">
          <a class="catalog_menu-link catalog_size-wide" href="#">
            <img class="catalog_img" src="/Catalog/catalog-1.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Молоко, сыр, яйцо</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-2.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Хлеб</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-3.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Овощи и фрукты</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-4.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Замороженные продукты</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-5.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Напитки</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-6.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Кондитерские изделия</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-7.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Чай, кофе</p>
          </a>

          <a class="catalog_menu-link catalog_size-wide" href="#">
            <img class="catalog_img" src="/Catalog/catalog-10.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Зоотовары</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-8.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Бакалея</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-9.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Здоровое питание</p>
          </a>

          <a class="catalog_menu-link catalog_size-wide" href="#">
            <img class="catalog_img" src="/Catalog/catalog-12.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Мясо, тица, колбаса</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-11.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Детское питание</p>
          </a>

          <a class="catalog_menu-link catalog_size-narrow" href="#">
            <img class="catalog_img" src="/Catalog/catalog-13.jpeg" alt="Молочка" />
            <div class="catalog_menu-gradient"></div>
            <p class="catalog_menu-title">Непродовольственные товары</p>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.catalog {
  position: relative;
}

.catalog_wrap {
  padding: 80px 0;
}

.catalog_size-wide {
  grid-column: 1/3;
  max-width: 584px;
}

.catalog_size-narrow {
  max-width: 272px;
}

.catalog_title {
  font-size: 64px;
  font-weight: 700;
}

.catalog_menu {
  margin-top: 60px;
  flex-wrap: wrap;
  gap: 40px;
  justify-content: space-between;
}

.catalog_menu-link {
  max-height: 200px;
  position: relative;
  border-radius: 4px;
  border: 1px solid transparent;
  box-shadow: rgba(255, 102, 51, 0.2);
  transition: 0.3s ease-in;
}

.catalog_img {
  border-radius: 4px;
}

.catalog_menu-link::before {
  content: '';
  position: absolute;
  left: 0;
  bottom: -1px;
  border-radius: 4px;
  width: 100%;
  height: 117px;
  background: linear-gradient(rgba(255, 102, 51, 0), rgb(255, 102, 51));
  transition: 0.3s ease-in;
}

.catalog_menu-link::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -1px;
  border-radius: 4px;
  width: 100%;
  height: 117px;
  background: linear-gradient(rgba(112, 192, 91, 0), rgb(112, 192, 91));
  transition: 0.3s ease-in;
}

.catalog_menu-link:hover::after {
  opacity: 0;
  transition: 0.3s ease-in;
}

.catalog_menu-title {
  position: absolute;
  left: 10px;
  bottom: 10px;
  font-size: 18px;
  font-weight: 700;
  color: white;
  z-index: 20;
}
</style>
