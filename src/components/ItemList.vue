<script setup>

import ItemCard from '@/components/ItemCard.vue'
import axios from 'axios'
import { onMounted, ref } from 'vue'

const items = ref([])
onMounted(async () => {
  try {
    const { data } = await axios.get('https://54cbfc4140ae6b3a.mokky.dev/items')
    items.value = data
  } catch (e) {
    console.log(e)
  }

})
</script>

<template>
  <div class="itemList">
    <h2 class="itemList_header">Все товары</h2>
    <div class="itemList_grid">
      <ItemCard
        v-for="item in items"
        :key="item.id"
        :title="item.title"
        :price="item.price"
        :image="item.image"
      />
    </div>
  </div>
</template>

<style scoped lang="scss">
.itemList {
  padding: 40px;

  &_grid {
    max-width: 100%;
    margin: 0 auto;
    margin-top: 20px;
    display: grid;
    gap: 40px;
  }

  &_header {
    color: #000;
    font-family: Inter, sans-serif;
    font-size: 32px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
  }
}

@media (min-width: 600px) {
  .itemList_grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 900px) {
  .itemList_grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (min-width: 1200px) {
  .itemList_grid {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>