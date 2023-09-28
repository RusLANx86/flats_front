<template>
  <div class="card relative z-2">
    <my-menu/>
  </div>
  <div class="grid">
    <div class="col-2 card">
      <left-panel/>
    </div>
    <div class="col-10">
      <my-table/>
    </div>
  </div>



</template>

<script setup>
import myMenu from "@/components/MyMenu.vue"
import leftPanel from "@/components/LeftPanel.vue"
import MyTable from "@/components/MyTable.vue";
</script>
