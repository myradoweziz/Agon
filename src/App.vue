<script setup>
  import TheHeader from '@/components/TheHeader.vue'
  import TheMain from '@/components/TheMain.vue'
  import SmartTehnologies from '@/components/SmartTehnologies.vue'
  import TehnologyProducts from '@/components/TehnologyProducts.vue'
  import ByCategories from '@/components/ByCategories.vue'
  import CrossBorder from '@/components/CrossBorder.vue'
  import NewsLetter from '@/components/NewsLetter.vue'
  import GetAccount from '@/components/GetAccount.vue'
  import TheFooter from '@/components/TheFooter.vue'
</script>
<template>
  <div class="wrapper">
    <the-header />
    <the-main />
    <smart-tehnologies />
    <tehnology-products />
    <by-categories />
    <cross-border />
    <news-letter />
    <get-account />
    <the-footer />
  </div>
</template>

<style scoped>
  .wrapper {
    padding: 5px 10px;
  }
</style>
