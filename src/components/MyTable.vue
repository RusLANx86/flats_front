
<template>

  <div class="card">
    <DataTable :value="products" tableStyle="min-width: 50rem">
      <template #header>
        <div class="flex flex-wrap align-items-center justify-content-between gap-2">
          <span class="text-xl text-900 font-bold">Products</span>
          <my-button icon="pi pi-refresh" rounded raised />
        </div>
      </template>
      <my-column field="name" header="Name"></my-column>
      <my-column header="Image">
        <template #body="slotProps">
          <img :src="`https://primefaces.org/cdn/primevue/images/product/${slotProps.data.image}`" :alt="slotProps.data.image" class="w-6rem shadow-2 border-round" />
        </template>
      </my-column>
      <my-column field="price" header="Price">
        <template #body="slotProps">
          {{ formatCurrency(slotProps.data.price) }}
        </template>
      </my-column>
      <my-column field="category" header="Category"></my-column>
      <my-column field="rating" header="Reviews">
        <template #body="slotProps">
          <my-rating :modelValue="slotProps.data.rating" readonly :cancel="false" />
        </template>
      </my-column>
      <my-column header="Status">
        <template #body="slotProps">
          <my-tag :value="slotProps.data.inventoryStatus" :severity="getSeverity(slotProps.data)" />
        </template>
      </my-column>
      <template #footer> In total there are {{ products ? products.length : 0 }} products. </template>
    </DataTable>
  </div>

</template>

<script setup>
import { ref, onMounted } from 'vue';
import { ProductService } from '@/service/ProductService';

onMounted(() => {
  ProductService.getProductsMini().then((data) => (products.value = data));
});

const products = ref();
const formatCurrency = (value) => {
  return value.toLocaleString('en-US', { style: 'currency', currency: 'USD' });
};
const getSeverity = (product) => {
  switch (product.inventoryStatus) {
    case 'INSTOCK':
      return 'success';

    case 'LOWSTOCK':
      return 'warning';

    case 'OUTOFSTOCK':
      return 'danger';

    default:
      return null;
  }
};


</script>