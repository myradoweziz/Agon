<script setup>
  import ButtonAll from './base/ButtonAll.vue'
  import AgonLogo from './base/AgonLogo.vue'

  const buttonProperties = [
    { id: 0, title: 'Ready to get started?' },
    { id: 1, title: 'Create an Account', isPrimary: true, icon: 'arrowRight', radius: '38' }
  ]
</script>

<template>
  <div class="account">
    <div class="account__container">
      <div class="account__row">
        <agon-logo />
        <div class="account__btns">
          <button-all
            v-for="buttonProperty in buttonProperties"
            :key="buttonProperty.id"
            :title="buttonProperty.title"
            :primary-btn="buttonProperty.isPrimary"
            :icon-name="buttonProperty.icon"
            :radius-btn="buttonProperty.radius"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .account {
    padding-bottom: 40px;
    @media (max-width: 479px) {
      padding-bottom: 30px;
    }
    &__container {
      border-bottom: 2px solid #d6d8dd;
      max-width: 1240px;
      margin: 0 auto;
      padding: 0 10px;
      overflow: hidden;
      padding-bottom: 50px;
    }
    &__row {
      padding-top: 30px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      @media (max-width: 594px) {
        flex-direction: column;
        flex-wrap: wrap;
      }
    }
    &__btns {
      display: flex;
      align-items: center;
      @media (max-width: 492px) {
        padding-top: 10px;
        flex-direction: column;
        flex-wrap: wrap;
      }
    }
  }
</style>
