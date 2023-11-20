<script setup>
  import BaseIcon from './BaseIcon.vue'

  const menus = [
    {
      id: 1,
      title: 'About Us',
      children: 'About V1',
      child: 'About V2',
      numbers: 'About V3',
      name: 'Services V2',
      place: 'Services V1'
    },
    {
      id: 2,
      title: 'Discover',
      children: 'Our Blog',
      child: 'Our Blog V1',
      numbers: 'Our Blog V2',
      place: 'Blog Single',
      name: 'Page 404'
    },
    {
      id: 3,
      title: 'Support',
      children: 'FAQs',
      child: 'FAQ V2',
      numbers: 'Career',
      place: 'Career Detail',
      name: 'Contact Us'
    },
    {
      id: 4,
      title: 'Useful links',
      children: 'Shop',
      child: 'Shop V2',
      numbers: 'Pricing V1',
      place: 'Pricing V2',
      name: 'Terms & Conditions'
    }
  ]

  const icons = ['facebook', 'instagram', 'twitter', 'in']

  const contactItems = [
    {
      title: 'Contact',
      contactSubItems: [
        { name: '4517 Washington Ave.' },
        { name: 'Manchester, Kentucky 3949' },
        { name: '(239) 555-0108' },
        { name: 'contact@agon.com', isBlueLink: true }
      ]
    }
  ]
</script>

<template>
  <div class="footer">
    <div class="footer__container">
      <div class="footer__row">
        <div class="footer__body">
          <ul class="footer__list">
            <li v-for="(contactItem, index) in contactItems" :key="index" class="footer__item">
              <div class="footer__title">{{ contactItem.title }}</div>
              <ul class="footer__sub-list">
                <li v-for="item in contactItem.contactSubItems" :key="item.name" class="footer__sub-item">
                  <a href="" :class="['footer__link', { blue: item.isBlueLink }]">{{ item.name }}</a>
                </li>
                <li class="footer__sub-item">
                  <div class="icons">
                    <a v-for="item in icons" :key="item" href="" class="footer__link">
                      <base-icon :name="item" />
                    </a>
                  </div>
                </li>
              </ul>
            </li>
            <li v-for="menu in menus" :key="menu.id" class="footer__item">
              <div class="footer__title">{{ menu.title }}</div>
              <ul class="footer__sub-list">
                <li class="footer__sub-item">
                  <a href="" class="footer__link"> {{ menu.children }}</a>
                </li>
                <li class="footer__sub-item">
                  <a href="" class="footer__link"> {{ menu.child }} </a>
                </li>
                <li class="footer__sub-item">
                  <a href="" class="footer__link">{{ menu.numbers }}</a>
                </li>
                <li class="footer__sub-item">
                  <a href="" class="footer__link">{{ menu.place }}</a>
                </li>
                <li class="footer__sub-item">
                  <a href="" class="footer__link">{{ menu.name }}</a>
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer__bottom">
        <div class="footer__company-seria">©Agon Official 2022</div>
        <div class="footer__sub-title">
          <p>Privacy policy</p>
          <span> Cookies </span>
          <p>Terms of service</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .footer {
    &__container {
      max-width: 1240px;
      margin: 0 auto;
      padding: 0 10px;
      overflow: hidden;
    }
    &__row {
      padding-bottom: 45px;
      @media (max-width: 450px) {
        padding-bottom: 15px;
      }
    }
    &__body {
    }
    &__title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 500;
      font-size: 18px;
      line-height: 26px;
      color: #101828;
      padding-bottom: 10px;
    }
    &__list,
    &__sub-list {
      list-style: none;
      padding: 0;
    }
    &__list {
      display: flex;
      justify-content: space-between;
      gap: 30px;
      @media (max-width: 900px) {
        flex-wrap: wrap;
      }
      @media (max-width: 600px) {
        justify-content: flex-start;
      }
    }
    &__sub-list {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    &__item {
    }
    &__link {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 24px;
      letter-spacing: 0.02em;
      color: #969696;
      text-decoration: none;
      &:hover {
        border-bottom: 2px solid #d6d8dd;
        padding-bottom: 3px;
      }
      &.blue {
        color: #4bb4ff;
        &:hover {
          border-bottom: 2px solid #4bb4ff;
          padding-bottom: 3px;
        }
      }
    }
    &__bottom {
      border-top: 2px solid #d6d8dd;
      padding: 25px 0;
      display: flex;
      align-items: center;
      justify-content: space-between;
      @media (max-width: 540px) {
        flex-wrap: wrap;
        flex-direction: column;
        padding: 10px 0;
        padding-bottom: 5px;
      }
    }
    &__company-seria {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 500;
      font-size: 18px;
      line-height: 26px;
      color: #969696;
    }
    &__sub-title {
      display: flex;
      align-items: center;
      gap: 10px;
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 24px;
      letter-spacing: 0.02em;
      color: #969696;
      p {
        margin: 0;
      }
      @media (max-width: 350px) {
        font-size: 12px;
      }
    }
  }
  .icons {
    display: flex;
    align-items: center;
    gap: 20px;
  }
</style>
