<script setup>

</script>

<template>
  <div class="header">
    <div class="header_item">
      <img src="/logo.png" alt="logo" class="header_logo">
      <h2 class="header_title">FitTreat</h2>
    </div>
    <div class="header_item">
      <img src="/cart.svg" alt="cart" class="header_cart">
    </div>
  </div>
</template>

<style scoped lang="scss">
.header{
  height: 128px;
  border-bottom: 2px solid #FFF4E7;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40px;
  &_item{
    display: flex;
    align-items: center;
    gap: 10px;
  }
  &_logo{
    width: 40px;
    height: 40px;
    cursor: pointer;
  }
  &_title{
    color: #000;
    font-family: Inter, sans-serif;
    font-size: 26px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    text-transform: capitalize;
    cursor: pointer;
  }
  &_cart{
    width: 40px;
    height: 40px;
    cursor: pointer;
  }
}
</style>