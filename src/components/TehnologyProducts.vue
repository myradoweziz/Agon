<script setup>
  import ButtonAll from './base/ButtonAll.vue'
  import BaseIcon from './BaseIcon.vue'

  const products = [
    { img: 'smart-watch.png', title: '4K TV Game Mini Arcade Rocker Console 32GB/64GB', name: 'Sony', count: '$29.80' },
    { img: 'head_music.png', title: 'Cancelling Headset Music Sport Deep Bass', name: 'Google', count: '$39.80' },
    {
      skidka: '-10',
      img: 'head_sead.png',
      title: 'T500BT Original Wireless Bluetooth Headphone',
      name: 'Toshiba',
      count: '$39.80'
    },
    {
      skidka: '-10',
      img: 'walnut_wood.png',
      title: 'Black Walnut Wood & Aluminum Headphone Stand',
      name: 'Toshiba',
      count: '$70.80'
    },
    {
      skidka: '-10',
      img: 'beatsBluetooth.png',
      title: 'Black Walnut Wood & Aluminum Headphone Stand',
      name: 'Toshiba',
      count: '$70.80'
    },
    {
      skidka: '-10',
      img: 'major3.png',
      title: 'Black Walnut Wood & Aluminum Headphone Stand',
      name: 'Toshiba',
      count: '$70.80'
    },
    { img: 'tbOrginal.png', title: 'Black Walnut Wood & Aluminum Headphone Stand', name: 'Toshiba', count: '$70.80' },
    {
      img: 'blueNaushnik.png',
      title: 'Black Walnut Wood & Aluminum Headphone Stand',
      name: 'Toshiba',
      count: '$70.80'
    },
    {
      skidka: '-10',
      img: 'beats-studio.png',
      title: 'Black Walnut Wood & Aluminum Headphone Stand',
      name: 'Toshiba',
      count: '$70.80'
    },
    {
      skidka: '-10',
      img: 'major.png',
      title: 'Black Walnut Wood & Aluminum Headphone Stand',
      name: 'Toshiba',
      count: '$70.80'
    },
    { img: 't5boot.png', title: 'Black Walnut Wood & Aluminum Headphone Stand', name: 'Toshiba', count: '$70.80' },
    { img: 'blackStand.png', title: 'Black Walnut Wood & Aluminum Headphone Stand', name: 'Toshiba', count: '$70.80' }
  ]

  const starIcons = ['fullStar', 'fullStar', 'fullStar', 'fullStar', 'halfStart']
</script>
<template>
  <div class="products">
    <div class="products__container">
      <div class="products__title">
        Featured Products <br />
        For Pre-Order
      </div>
      <div class="products__columns">
        <div v-for="item in products" :key="item.name" class="products__box">
          <div class="product__count">
            <span>{{ item.skidka }}</span>
          </div>
          <a href="" class="products__image">
            <img :src="require(`@/assets/img/products/${item.img}`)" alt="" />
          </a>
          <a href="" class="products__name">{{ item.name }}</a>
          <a href="" class="products__box-title">{{ item.title }}</a>
          <div class="products__level">
            <base-icon v-for="icon in starIcons" :key="icon" :name="icon" />
          </div>
          <div class="products__count-btn">
            <div class="products__count">{{ item.count }}</div>
            <div class="products__btn">
              <button-all title="Add +" blue-color radius-btn="6" width-btn="67" height-btn="23" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .products {
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
    &__title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      font-size: 50px;
      line-height: 60px;
      color: #101828;
      padding-bottom: 50px;
      text-align: center;
      @media (max-width: 514px) {
        font-size: 40px;
        line-height: 45px;
        padding-bottom: 20px;
      }
      @media (max-width: 370px) {
        font-size: 28px;
      }
    }
    &__columns {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
      @media (max-width: 992px) {
        grid-template-columns: repeat(2, 1fr);
      }
      @media (max-width: 462px) {
        grid-template-columns: repeat(1, 1fr);
      }
    }
    &__box-title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      font-size: 16px;
      line-height: 26px;
      color: #323a4b;
      padding-bottom: 8px;
    }
    &__box {
      display: flex;
      flex-direction: column;
      padding: 25px 15px;
      border: 1px solid #e4e7ec;
      box-shadow: 0px 0px 1px 1px rgba(228, 231, 236, 0.15);
      border-radius: 6px;
      a {
        text-decoration: none;
      }
    }
    &__image {
      text-align: center;
      padding-top: 20px;
      flex: 1 1 auto;
    }
    &__name {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 400;
      font-size: 12px;
      line-height: 26px;
      color: #576071;
      padding-bottom: 4px;
    }
    &__level {
      display: flex;
      align-items: center;
      gap: 2px;
      padding-bottom: 16px;
    }
    &__count-btn {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    &__count {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      font-size: 18px;
      line-height: 26px;
      color: #006d77;
    }
  }

  .product__count {
    background: #101828;
    border-radius: 25px;
    color: #fff;
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 400;
    font-size: 10px;
    line-height: 15px;
    max-width: 39px;
    text-align: center;
  }
</style>
