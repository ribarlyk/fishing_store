<template>
  <div class="text-center">
    <v-menu open-on-hover>
      <template v-slot:activator="{ props }">
        <v-btn class="custom-button" v-bind="props" :title="title">
          {{ title }}
        </v-btn>
      </template>

      <v-list>
        <v-list-item v-for="(item, index) in items" :key="index">
          <v-list-item-title class="item">{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>

<script setup lang="ts">
defineProps({
  title: [],
});

const items = ref([
  { title: "Click Me" },
  { title: "Click Me" },
  { title: "Click Me" },
  { title: "Click Me 2" },
  { title: "Click Me 2" },
  { title: "Click Me 2" },
  { title: "Click Me 2" },
]);
</script>

<style scoped>
.custom-button {
  background-color: transparent;
  color: white;
  border: none;
  box-shadow: none;
}
.custom-button:hover {
  background-color: transparent;

  color: #e2bd36;
}

.item:hover {
  color: #e2bd36;
  cursor: pointer;
}
</style>
