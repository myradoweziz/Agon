<script setup>
import { defineProps } from 'vue'
import BaseIcon from '../BaseIcon.vue'
const props = defineProps({
  icon: {
    type: String,
    default: () => ''
  },
  title: {
    type: String,
    default: () => ''
  },
  firstName: {
    type: String,
    default: () => ''
  },
  lastName: {
    type: String,
    default: () => ''
  },
  bgColor: {
    type: String,
    default: () => ''
  }
})
</script>
<template>
  <div :style="`background: ${props.bgColor} `" class="cross__item">
    <div class="cross__image">
      <BaseIcon :name="props.icon" />
    </div>
    <div class="cross__sub-title">{{ props.title }}</div>
    <div class="cross__description">
      {{ props.firstName }}<br />
      {{ props.lastName }}
    </div>
  </div>
</template>

<style lang="scss" scoped>
.cross {
  &__item {
    padding: 40px 70px 45px 70px;
    border-radius: 8px;
    &:nth-child(5) {
      padding: 40px 90px 45px 90px;
      background: #dbece5;
    }
    br {
      @media (max-width: 350px) {
        display: none;
      }
    }
  }

  &__description {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 26px;
    text-align: center;
    color: #667085;
  }
  &__sub-title {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 32px;
    line-height: 33px;
    color: #1e2534;
    padding-top: 22px;
    padding-bottom: 30px;
    text-align: center;
    @media (max-width: 350px) {
      font-size: 25px;
      padding-bottom: 10px;
    }
  }
}
</style>
