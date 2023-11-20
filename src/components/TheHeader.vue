<script setup>
  import { ref } from 'vue'

  import AgonLogo from '@/components/base/AgonLogo.vue'
  import ButtonAll from './base/ButtonAll.vue'
  import BaseIcon from './BaseIcon.vue'

  const activeBurger = ref(false)

  const menuItems = [
    { id: 0, title: 'Home', activeClass: true },
    { id: 1, title: 'About' },
    { id: 2, title: 'Company' },
    { id: 3, title: 'Pages' },
    { id: 4, title: 'Blog' },
    { id: 5, title: 'Shop' }
  ]
</script>
<template>
  <div :class="['header', { active: activeBurger }]">
    <div class="header__container">
      <div class="header__row">
        <div class="header__logo">
          <agon-logo />
        </div>
        <div class="header__body">
          <ul class="header__menu">
            <li v-for="item in menuItems" :key="item.title" class="header__item">
              <a href="" :class="['header__link ', { active_item: item.activeClass }]">
                {{ item.title }}
              </a>
            </li>
          </ul>
        </div>
        <div class="header__btn-burg">
          <div class="header__btn">
            <button-all title="Get Started" primary-btn radiusBtn="47" />
          </div>
          <div class="header__burger" @click="activeBurger = !activeBurger">
            <base-icon :name="activeBurger ? 'close' : 'burger'" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .header {
    min-height: 100px;
    position: relative;
    padding-bottom: 100px;
    @media (max-width: 972px) {
      padding-bottom: 0;
    }
    @media (max-width: 450px) {
      padding: 30px 0;
    }
    &.active {
      .header__logo {
        @media (max-width: 850px) {
          display: none;
        }
      }
      .header {
        background-color: #fff;
      }

      .header__body {
        @media (max-width: 850px) {
          left: 0;
          transition: left 0.3s;
        }
      }
      .header__menu {
        @media (max-width: 850px) {
          padding-top: 50px;
          display: flex;
          flex-direction: column;
          align-items: center;
          z-index: 3;
          gap: 20px;
        }
      }
      .header__link {
        font-size: 20px;
      }
      .header__btn {
        @media (max-width: 850px) {
          display: none;
        }
      }
    }
    &__container {
      max-width: 1240px;
      margin: 0 auto;
      overflow: hidden;
      padding: 0 10px;
    }
    &__btn-burg {
      display: flex;
      align-items: center;
      gap: 20px;
      padding: 10px 0;
    }
    &__burger {
      display: none;
      @media (max-width: 850px) {
        display: inline;
        position: relative;
        z-index: 10;
      }
    }
    &__logo {
      @media (max-width: 350px) {
        width: 80px;
      }
    }
    &__row {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    &__body {
      @media (max-width: 850px) {
        position: fixed;
        width: 100%;
        left: -100%;
        transition: left 0.3s ease 0s;
        top: 0;
        background-color: #fff;
        height: 100%;
        z-index: 2;
      }
    }

    &__menu {
      display: flex;
      align-items: center;
      gap: 30px;
      list-style: none;
      padding: 0;
      @media (max-width: 850px) {
        display: none;
      }
    }

    &__link {
      &.active_item {
        color: #006d77;
        border: none;
        &:hover {
          border-bottom: 1px solid #006d77;
        }
      }
      &:hover {
        border-bottom: 1px solid #101828;
      }
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 500;
      font-size: 16px;
      line-height: 26px;
      letter-spacing: 0.045em;
      text-decoration: none;
      color: #101828;
    }
    &__btn {
      button {
        @media (max-width: 350px) {
          font-size: 12px;
          padding-top: 8px;
          padding-bottom: 8px;
        }
      }
    }
  }
</style>
