<template>
  <div class="input-container" :class="{ focused: containerIsFocused }">
    <input
      type="text"
      class="input-field"
      placeholder="Търсене на продукти..."
      @focus="containerIsFocused = true"
      @blur="containerIsFocused = false"
    />
    <button class="icon-container" @click="onSearch">
      <nuxt-icon name="magnifying" class="top-bar-icons" />
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const containerIsFocused = ref(false);

const onSearch = () => {
  console.log();
};
</script>

<style scoped>
.input-container {
  display: flex;
  align-items: center;
  border: 1px solid #8a8686;
  background-color: rgb(82, 131, 223);
  height: 3rem;
  border-radius: 2rem;
  padding-left: 20px;
  transition: border-color 0.3s;
  width: 35rem;
}

.input-container.focused {
  border-color: #ffffff;
}

.input-field {
  border: none;
  background-color: transparent;
  caret-color: white;
  flex: 1;
  outline: none;
  color: #ffffff;
  padding: 0.5em;
}

.input-field::placeholder {
  color: #ffffff;
  font-size: 0.9em;
}

.icon-container {
  background-color: transparent;
  border: none;
  cursor: pointer;
  padding: 0;
}

button {
  height: 2.85rem;
  width: 3rem;
}

button:hover {
  background-color: #e2bd36;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
}

.top-bar-icons {
  color: white;
}

@media screen and (max-width: 768px) {
  .input-container {
    height: 2rem;
    padding: 10px;
    width: 100%;
  }

  .input-field::placeholder {
    font-size: 0.8em;
  }

  .icon-container {
    padding: 0.5rem;
  }
}
</style>
