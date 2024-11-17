<template>
  <div class="header">
    <div class="container">
      <div class="header_wrap flex">
        <img src="/logo.svg" alt="Логотип" />

        <a href="#" class="header_button flex">
          <img src="/burger.svg" alt="Бургер" />
          <p>Каталог</p>
        </a>

        <div class="header_input-group">
          <input class="header_input" type="search" placeholder="Найти товар" />
          <button class="header_input__btn" type="button">
            <img src="/search.svg" alt="Поиск" />
          </button>
        </div>

        <div class="header_nav flex">
          <a href="#" class="header_nav-icon flex">
            <img src="/favrites.svg" alt="Избранное" />
            <p>Избранное</p>
          </a>
          <a href="#" class="header_nav-icon flex">
            <img src="/orders.svg" alt="Заказы" />
            <p>Заказы</p>
          </a>
          <a href="#" class="header_nav-icon flex">
            <img src="/cart.svg" alt="Корзина" />
            <p>Корзина</p>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header {
  width: 100%;
  background-color: white;
}

.header_wrap {
  height: 72px;
  justify-content: space-between;
  align-items: center;
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

.header_input-group {
  position: relative;
}

.header_input {
  width: 375px;
  height: 40px;
  font-family: inherit;
  position: relative;
  padding: 8px 42px 8px 16px;
  border-radius: 4px;
  border: 1.5px solid #70c05b;
  background-color: transparent;
  color: #8f8f8f;
  font-size: 16px;
}

.header_input__btn {
  position: absolute;
  top: 6px;
  right: 0;
  border: none;
  background-color: transparent;
  cursor: pointer;
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
  color: rgb(65, 65, 65);
}

.header_nav-icon:not(:last-child) {
  margin-right: 24px;
}
</style>
