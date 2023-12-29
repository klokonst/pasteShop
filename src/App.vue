<script setup>

import MainHeader from '@/components/MainHeader.vue'
import ItemList from '@/components/ItemList.vue'
</script>

<template>
  <div class="appWrapper">
    <MainHeader/>
    <ItemList/>
  </div>
</template>

<style lang="scss" scoped>
.appWrapper {
  max-width: 1080px;
  margin: auto;
  margin-top: 10px;
  margin-bottom: 10px;
  background-color: white;
  border-radius: 20px;
}
</style>