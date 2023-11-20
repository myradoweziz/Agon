<script setup>
  import BaseIcon from './BaseIcon.vue'

  const categories = [
    { icon: 'comp', title: 'Computer for Designer, Art' },
    { icon: 'laptop', title: 'Sport, Home, Outdoor' },
    { icon: 'laptop', title: 'Laptop for office, students' },
    { icon: 'software', title: 'Software, card, book' }
  ]

  const persons = [
    { title: 'Computer - Laaptop', count: 10 },
    { title: 'Smart phone & Tablets', count: 12 },
    { title: 'Fashion & Accessories', count: 14 },
    { title: 'Halth & Beauty', count: 8 }
  ]
</script>

<template>
  <div class="categories">
    <div class="categories__contianer">
      <div class="categories__sub-content">
        <div class="categories__title">Explore by Categories.</div>
        <div class="categories__sub-title">
          We provide many categories, choose a category according to <br />
          your expertise to make it easier to find a job.
        </div>
      </div>
      <div class="categories__popular-design">
        <div class="categories__popular popular_categories">
          <div class="popular_categories__title">Popular Categories</div>
          <div v-for="person in persons" :key="person.title" class="popular_categories__row">
            <p>{{ person.title }}</p>
            <span>{{ person.count }}</span>
          </div>
        </div>
        <div>
          <div class="categories__health-design">
            <div v-for="item in categories" :key="item.title" class="categories__body">
              <div class="categories__image">
                <base-icon :name="item.icon" />
              </div>
              <div class="categories__com-title">{{ item.title }}</div>
            </div>
          </div>
          <div>
            <div class="categories__body_last">
              <div class="categories__image">
                <base-icon name="explore" />
              </div>
              <div class="categories__com-title">Explore More</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .categories {
    padding-bottom: 100px;
    @media (max-width: 479px) {
      padding-bottom: 30px;
    }
    &__contianer {
      max-width: 1240px;
      margin: 0 auto;
      padding: 0 10px;
      overflow: hidden;
    }
    &__sub-content {
      text-align: center;
      padding-bottom: 50px;
    }
    &__title {
      padding-bottom: 25px;
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      font-size: 50px;
      line-height: 60px;
      color: #101828;
      @media (max-width: 605px) {
        font-size: 38px;
        line-height: 40px;
      }
      @media (max-width: 350px) {
        font-size: 30px;
      }
    }
    &__sub-title {
      font-family: 'Merriweather';
      font-style: normal;
      font-weight: 400;
      font-size: 16px;
      line-height: 26px;
      letter-spacing: 0.045em;
      color: #475467;
      @media (max-width: 450px) {
        font-size: 15px;
      }
    }
    &__popular-design {
      display: flex;
      gap: 50px;
      @media (max-width: 750px) {
        flex-direction: column;
        flex-wrap: wrap;
      }
    }
    &__popular {
      flex: 0 0 30%;
      background: #ffffff;
      border: 1px solid #d1dae8;
      box-shadow: 0px 3px 6px rgba(219, 220, 222, 0.17);
      border-radius: 6px;
      padding: 25px;
    }
    &__health-design {
      display: grid;
      gap: 30px;
      grid-template-columns: repeat(2, 1fr);
      &:not(:last-child) {
        margin-bottom: 30px;
      }
      @media (max-width: 992px) {
        grid-template-columns: 1fr;
        gap: 20px;
      }
    }
    &__body {
      display: flex;
      align-items: center;
      gap: 13px;
      padding: 10px 50px;
      background: #ffffff;
      border: 1px solid #d1dae8;
      border-radius: 6px;
      max-height: 96px;
      @media (max-width: 400px) {
        padding: 10px;
      }
    }

    &__body-row {
      display: flex;
    }
    &__body_last {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 13px;
      background: #ffffff;
      border: 1px solid #d1dae8;
      border-radius: 6px;
      margin: 0px auto;
      padding: 12px;
      @media (max-width: 992px) {
        padding: 10px;
        justify-content: flex-start;
        margin: 0;
        padding-left: 60px;
      }
      @media (max-width: 350px) {
        padding-left: 18px;
      }
    }
    &__image {
    }
    &__com-title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      font-size: 14px;
      line-height: 26px;
      color: #323a4b;
      @media (max-width: 350px) {
        font-size: 13px;
      }
    }
  }

  .popular_categories {
    &__title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      font-size: 29px;
      line-height: 33px;
      color: #323a4b;
      padding-bottom: 40px;
      @media (max-width: 375px) {
        font-size: 22px;
        padding-bottom: 10px;
      }
    }
    &__row {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 10px 0;
      justify-content: space-between;
      border-bottom: 1px solid #e4e7ec;
      p {
        font-family: 'Work Sans';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 26px;
        color: #667085;
      }
      span {
        padding: 5px 12px;
        border-radius: 50px;
        font-family: 'Work Sans';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 26px;
        color: #006d77;
        background-color: #e4e7ec;
      }
    }
  }
</style>
