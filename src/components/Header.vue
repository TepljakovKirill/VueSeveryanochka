<template>
  <div class="header_wrap container flex">
    <img src="/logo.svg" alt="Логотип" />

    <a href="#" class="header_button flex">
      <img src="/burger.svg" alt="Бургер" />
      <a href="#">Каталог</a>
    </a>

    <input class="header_input" type="search" placeholder="Найти товар" />
    <div class="header_nav flex">
      <div class="header_nav-icon flex">
        <img src="/favrites.svg" alt="Избранное" />
        <p>Избранное</p>
      </div>
      <div class="header_nav-icon flex">
        <img src="/orders.svg" alt="Заказы" />
        <p>Заказы</p>
      </div>
      <div class="header_nav-icon flex">
        <img src="/cart.svg" alt="Корзина" />
        <p>Корзина</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header_wrap {
  height: 72px;
  align-items: center;
  justify-content: space-between;
  background-color: white;
}

.header_button {
  width: 140px;
  height: 40px;
  justify-content: space-between;
  align-items: center;
  border-radius: 4px;
  background-color: #70c05b;
  transition: 0.3s ease-in;
}

.header_button:hover {
  background-color: #88d375;
  transition: 0.3s ease-in;
}

.header_button img {
  width: 24px;
  height: 24px;
  margin-left: 10px;
}

.header_button p {
  color: white;
  margin-right: 22px;
}

.header_input {
  width: 375px;
  height: 40px;
  font-family: inherit;

  background-image: url(./search.svg);
  background-position: calc(100% - 6px) center;
  background-repeat: no-repeat;

  position: relative;
  padding: 8px 42px 8px 16px;
  border-radius: 4px;
  border: 1.5px solid #70c05b;
  background-color: transparent;
  color: #8f8f8f;
  font-size: 16px;
}

.header_input:focus {
  border: 2px solid #70c05b;
  outline: none;
}

.header_nav-icon {
  height: 50px;
  font-size: 12px;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.header_nav-icon:not(:last-child) {
  margin-right: 24px;
}
</style>
