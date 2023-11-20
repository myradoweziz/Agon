<script setup>
  const technologyProducts = [
    { img: 'television.png', productName: '4K TV Game Mini Arcade Rocker Console 32GB/64GB ', count: '$29.80' },
    { img: 'deep_music.png', productName: 'Cancelling Headset Music Sport Deep Bass ', count: '$420.00' },
    { img: 'headphone.png', productName: 'T500BT Original Wireless Bluetooth Headphone Deep ', count: '$96.50' }
  ]
</script>
<template>
  <div class="smart">
    <div class="smart__container">
      <div class="smart__row">
        <div v-for="(product, index) in technologyProducts" :key="index" class="smart__body">
          <div class="smart__image">
            <img :src="require(`@/assets/img/${product.img}`)" alt="" />
          </div>
          <div class="smart__title">
            <span> {{ product.productName }}</span>
            <p class="smart__count">{{ product.count }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .smart {
    padding-bottom: 100px;
    @media (max-width: 479px) {
      padding-bottom: 30px;
    }
    &__container {
      max-width: 1240px;
      margin: 0 auto;
      padding: 0 10px;
      overflow: hidden;
    }
    &__row {
      display: flex;
      align-items: center;
      justify-content: space-around;
      gap: 30px;
      @media (max-width: 1140px) {
        flex-wrap: wrap;
      }
    }
    &__body {
      padding: 25px;
      border: 1px solid #e4e7ec;
      box-shadow: 0px 0px 1px 1px rgba(228, 231, 236, 0.15);
      border-radius: 6px;
      display: flex;
      gap: 20px;
      max-width: 350px;
      @media (max-width: 890px) {
        flex-direction: column;
      }
    }
    &__image {
      @media (max-width: 890px) {
        text-align: center;
      }
    }
    &__title {
      line-height: 20px;
      span {
        font-family: 'Work Sans';
        font-style: normal;
        font-weight: 600;
        font-size: 16px;
        color: #323a4b;
        @media (max-width: 450px) {
          font-size: 15px;
        }
      }
    }
    &__count {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 300;
      font-size: 16px;
      color: #101828;
    }
  }
</style>
