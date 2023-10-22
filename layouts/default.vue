<template>
  <div>
    <div class="header-container">
      <div class="top-bar header-bar">
        <div>
          <ul class="top-bar-left-list">
            <li class="top-bar-li-item">
              <nuxt-icon name="house" class="top-bar-icons"></nuxt-icon>
              <NuxtLink to="/za-nas" class="link">За Нас</NuxtLink>
            </li>
            <li class="top-bar-li-item">
              <nuxt-icon name="percent" class="top-bar-icons"></nuxt-icon>
              <NuxtLink to="/promocii" class="link">Промоции</NuxtLink>
            </li>
            <li class="top-bar-li-item">
              <nuxt-icon name="truck" class="top-bar-icons"></nuxt-icon>
              <NuxtLink to="/informaciq-za-dostavka" class="link"
                >Информация за Доставка</NuxtLink
              >
            </li>
            <li class="top-bar-li-item">
              <nuxt-icon name="envelope" class="top-bar-icons"></nuxt-icon>
              <NuxtLink to="/kontakti" class="link">Контакти</NuxtLink>
            </li>
          </ul>
        </div>
        <div class="top-bar-middle"></div>
        <div class="top-bar-right-list">
          <ul>
            <li>
              <NuxtLink to="https://facebook.com" target="_blank">
                <nuxt-icon name="facebook" class="top-bar-icons"></nuxt-icon>
              </NuxtLink>
            </li>
            <li>
              <NuxtLink to="https://instagram.com" target="_blank">
                <nuxt-icon name="instagram" class="top-bar-icons"></nuxt-icon>
              </NuxtLink>
            </li>
            <li>
              <nuxt-icon name="envelope" class="top-bar-icons" />
              <span class="contacts">test@test.bg</span>
            </li>
            <li><nuxt-icon name="phone" class="top-bar-icons" /></li>
            <span class="contacts">0897 13 12 19</span>
          </ul>
        </div>
      </div>

      <div class="middle-bar header-bar">
        <div class="logo-container">
          <NuxtLink to="https://instagram.com" target="_blank">
            <img src="../assets/logo/pngwing.com.png" alt="logo" class="logo" />
          </NuxtLink>
        </div>

        <div class="search-bar-container">
          <search-bar />
        </div>

        <div class="icons-container">
          <icon-list />
          <cart />
        </div>
      </div>
      <div class="bottom-bar header-bar">
        <menu-list />
      </div>
    </div>
    <slot />
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
ul {
  display: flex;
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.link,
.contacts {
  text-decoration: none;
  color: #fff;

}

.logo {
  max-width: 150px;
  height: 110px;
}

.link:hover {
  color: #e2bd36;
}

.header-bar {
  background-color: rgb(82, 131, 223);
}

.top-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 10rem;
  background-color: rgb(68, 115, 201);
}

.top-bar-icons {
  color: #e2bd36;
  margin: 0 10px;
}

.top-bar-middle {
  flex: 1;
}

.middle-bar {
  display: flex;
  align-items: center;
  justify-content: space-around;
  padding: 1rem 20rem;
}

.search-bar-container {
  display: flex;
  align-items: center;
}

.icons-container {
  display: flex;
}

.bottom-bar {
  background-color: rgb(68, 115, 201);
}
</style>
