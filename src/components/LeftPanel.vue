<script setup>
import {ref} from "vue";
const value = ref("");
const items = ref([]);

const search = (event) => {
  let _items = [...Array(10).keys()];

  items.value = event.query ? [...Array(10).keys()].map((item) => event.query + '-' + item) : _items;
}
</script>

<template>
  <AutoComplete v-model="value" dropdown :suggestions="items" @complete="search"/>
</template>

<style scoped>

</style>