<template>
  <div class="info-bar">
    <div class="delivery">
      <nuxt-icon name="truck" class="icon"></nuxt-icon>
      <div>
        <h4>Бърза доставка до цялата страна</h4>
        <h5>Доставка до цялата страна до 2 работни дни</h5>
      </div>
    </div>

    <div class="payment">
      <nuxt-icon name="money" class="icon"></nuxt-icon>
      <div>
        <h4>Сигурно Плащане</h4>
        <h5>Плащане след преглед</h5>
      </div>
    </div>

    <div class="support">
      <nuxt-icon name="phone" class="icon"></nuxt-icon>
      <div>
        <h4>Бързо обслужване по телефон и email</h4>
        <h5>Свържете се с нас и поръчайте</h5>
      </div>
    </div>
  </div>
</template>

<style scoped>
.info-bar {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 6rem;
  background-color: rgb(68, 115, 201);
  padding: 0.2rem;
}

.delivery,
.payment,
.support {
  display: flex;
  align-items: center;
  text-align: center;
}

.icon {
  font-size: 2rem;
  margin-right: 1rem;
  color: #e2bd36;
}

h4,
h5 {
  color: #ffffff;
}

@media screen and (max-width: 768px) {
  .info-bar {
    flex-direction: column;
    align-items: center;
  }

  .delivery,
  .payment,
  .support {
    flex-basis: 100%;
  }
  .icon {
    font-size: 1rem;
    margin-right: 0.5rem;
    color: #e2bd36;
  }
}
</style>
