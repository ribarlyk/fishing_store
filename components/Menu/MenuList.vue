<template>
  <ul>
    <li v-for="(item, index) in menuItems" :key="index">
      <Dropdown :title="item" />
    </li>
  </ul>
</template>

<script setup lang="ts">
const menuItems = ref([
  "ВЪДИЦИ",
  "МАКАРИ",
  "КУКИ",
  "ВЛАКНА",
  "ПРИМАМКИ",
  "ЗАХРАНКИ",
  "АКСЕСОАРИ",
  "КЪМПИНГ",
  "ШАРАНДЖЙИСКИ РИБОЛОВ",
  "ПРОМОЦИИ",
]);
</script>

<style scoped>
ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  list-style: none;
  padding: 0;
}

li {
  margin: 0.5rem;
}

@media (max-width: 768px) {
  ul {
    flex-direction: column;
    align-items: center;
  }
}
</style>
