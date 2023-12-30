<script setup>
defineProps({
  image: String
})
</script>

<template>
  <div class="itemCard">
    <img :src="image" alt="img" class="itemCard_img">
    <div class="itemCard_left"></div>
    <img src="/plus.svg" alt="btn" class="itemCard_button">
  </div>
</template>

<style scoped lang="scss">
.itemCard {
  width: 100%;
  height: 360px;
  border-radius: 40px;
  display: flex;
  box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px, rgba(0, 0, 0, 0.23) 0px 6px 6px;
  flex-direction: column;
  position: relative;

  &_left{
    position: absolute;
    left: 0;
    bottom: 0;
    height: 70%;
    width: 20%;
    background-color: white;
    border-radius: 0 40px 0 40px;
    box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px, rgba(0, 0, 0, 0.23) 0px 6px 6px;
  }

  &_img {
    width: 100%;
    height: 100%;
    border-radius: 40px;
  }

  &_button {
    position: absolute;
    border-radius: 100%;
    right: 10px;
    bottom: 10px;
    width: 64px;
    height: 64px;
    cursor: pointer;
    background-color: white;
    box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px, rgba(0, 0, 0, 0.23) 0px 6px 6px;
  }
}
</style>