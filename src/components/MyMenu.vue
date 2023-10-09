<script setup>
import {ref} from "vue";

const menu_items = ref([
  {
    label: 'Заказать решение',
    icon: 'pi pi-fw pi-file',
    items: [
      {
        label: 'Купить литературу',
        icon: 'pi pi-fw pi-plus',
        items: [
          {
            label: 'Bookmark',
            icon: 'pi pi-fw pi-bookmark'
          },
          {
            label: 'Video',
            icon: 'pi pi-fw pi-video'
          }
        ]
      },
      {
        label: 'Удалить',
        icon: 'pi pi-fw pi-trash'
      },
      {
        separator: true
      },
      {
        label: 'Export',
        icon: 'pi pi-fw pi-external-link'
      }
    ]
  },
  {
    label: 'Онлайн обучение',
    icon: 'pi pi-fw pi-pencil',
    items: [
      {
        label: 'Left',
        icon: 'pi pi-fw pi-align-left'
      },
      {
        label: 'Right',
        icon: 'pi pi-fw pi-align-right'
      },
      {
        label: 'Center',
        icon: 'pi pi-fw pi-align-center'
      },
      {
        label: 'Justify',
        icon: 'pi pi-fw pi-align-justify'
      }
    ]
  },
  {
    label: 'Самосевершенствование',
    icon: 'pi pi-fw pi-user',
    items: [
      {
        label: 'Новый',
        icon: 'pi pi-fw pi-user-plus'
      },
      {
        label: 'Удалить',
        icon: 'pi pi-fw pi-user-minus'
      },
      {
        label: 'Поиск',
        icon: 'pi pi-fw pi-users',
        items: [
          {
            label: 'Фильтр',
            icon: 'pi pi-fw pi-filter',
            items: [
              {
                label: 'Печать',
                icon: 'pi pi-fw pi-print'
              }
            ]
          },
          {
            icon: 'pi pi-fw pi-bars',
            label: 'Список'
          }
        ]
      }
    ]
  },
  {
    label: 'База задач',
    icon: 'pi pi-fw pi-calendar',
    items: [
      {
        label: 'Edit',
        icon: 'pi pi-fw pi-pencil',
        items: [
          {
            label: 'Save',
            icon: 'pi pi-fw pi-calendar-plus'
          },
          {
            label: 'Delete',
            icon: 'pi pi-fw pi-calendar-minus'
          }
        ]
      },
      {
        label: 'Archieve',
        icon: 'pi pi-fw pi-calendar-times',
        items: [
          {
            label: 'Remove',
            icon: 'pi pi-fw pi-calendar-minus'
          }
        ]
      }
    ]
  },
  {
    label: 'Статьи',
    icon: 'pi pi-fw pi-book'
  }
]);
</script>

<template>
    <my-menubar :model="menu_items" />
</template>

<style scoped>

</style>