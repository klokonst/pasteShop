<script setup>
defineProps({
  title: String,
  price: String,
  image: String
})
</script>

<template>
  <div class="itemCard">
    <img :src="image" alt="img" class="itemCard_img">
    <p class="itemCard_title">{{ title }}</p>
      <div class="itemCard_bottom">
        <div class="itemCard_price">
          <p class="itemCard_price_title">ЦЕНА:</p>
          <h3 class="itemCard_price_name">{{ price }}</h3>
        </div>
        <img src="/plus.svg" alt="btn" class="itemCard_button">
      </div>
  </div>
</template>

<style scoped lang="scss">
.itemCard {
  width: 100%;
  height: 260px;
  border-radius: 40px;
  border: 1px solid #F3F3F3;
  padding: 34px;
  padding-top: 20px;
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
  display: flex;
  flex-direction: column;

  &_img {
    display: block;
    width: 133px;
    height: 112px;
  }

  &_title {
    color: #000;
    font-family: Inter, sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    margin-top: 14px;
  }

  &_button {
    width: 32px;
    height: 32px;
    cursor: pointer;
  }

  &_bottom {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 14px;
  }

  &_price {
    &_title {
      color: #BDBDBD;
      font-family: Inter, sans-serif;
      font-size: 11px;
      font-style: normal;
      font-weight: 500;
      line-height: normal;
      text-transform: uppercase;
    }

    &_name {
      color: #000;
      font-family: Inter, sans-serif;
      font-size: 14px;
      font-style: normal;
      font-weight: 700;
      line-height: normal;
      margin-top: 2px;
    }
  }
}
</style>