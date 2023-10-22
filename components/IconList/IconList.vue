<template>
  <ul>
    <li>
      <div class="menu-item">
        <nuxt-icon name="user" class="icon" />
        <p>Вход</p>
      </div>
    </li>
    <li>
      <div class="menu-item">
        <nuxt-icon name="address" class="icon" />
        <p>Регистрация</p>
      </div>
    </li>
    <li>
      <div class="menu-item">
        <nuxt-icon name="heart" class="icon" />
        <p>Любими</p>
      </div>
    </li>
  </ul>
</template>

<style scoped>
.icon {
  font-size: 2rem;
}

.menu-item {
  display: flex;
  align-items: center;
  flex-direction: column;
  margin: 5px;
}

.menu-item,
.icon {
  transition: color 0.3s;
  color: #fff;

}

.menu-item:hover,
.menu-item:hover .icon {
  color: #e2bd36;
  cursor: pointer;
}
</style>
