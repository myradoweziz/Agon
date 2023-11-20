<script setup>
import BaseIcon from './BaseIcon.vue'
</script>
<template>
  <div class="news">
    <div class="news__contianer">
      <div class="news__row">
        <div class="news__content">
          <div class="news__title">Subscribe our newsletter</div>
          <div class="news__description">
            By clicking the button, you are agreeing with our Term & <br />
            Conditions
          </div>
          <div class="news__search">
            <input type="text" placeholder="Enter you mail..." />
            <span class="cursor">
              <BaseIcon name="searchArrow" />
            </span>
          </div>
        </div>
        <div class="news__box">
          <div class="news__image">
            <span>
              <img src="../assets/img/grafik.png" alt="" />
            </span>
            <img src="../assets/img/persons.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.news {
  padding-bottom: 100px;
  @media (max-width: 479px) {
    padding-bottom: 30px;
  }
  &__contianer {
    max-width: 1240px;
    margin: 0 auto;
    padding: 0 10px;
  }
  &__row {
    background: #006d77;
    box-shadow: 0px 7px 20px rgba(0, 0, 0, 0.15);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    @media (max-width: 1160px) {
      flex-wrap: wrap;
      flex-direction: column;
    }
  }
  &__content {
    padding: 50px;
    width: 100%;
    @media (max-width: 1160px) {
      padding: 15px;
      padding-bottom: 0;
    }
  }
  &__title {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 40px;
    line-height: 50px;
    color: #ffffff;
    padding-bottom: 11px;
    @media (max-width: 652px) {
      font-size: 35px;
    }
    @media (max-width: 450px) {
      font-size: 33px;
      line-height: 43px;
    }
  }
  &__description {
    padding-bottom: 20px;
    font-family: 'Merriweather';
    font-style: normal;
    font-weight: 300;
    font-size: 16px;
    line-height: 26px;
    letter-spacing: 0.045em;
    color: #ffffff;
    @media (max-width: 652px) {
      font-size: 15px;
      br {
        display: none;
      }
    }
    @media (max-width: 652px) {
      font-size: 13px;
    }
  }
  &__search {
    position: relative;
    width: 100%;
    input {
      background: #ffffff;
      outline: none;
      border: none;
      box-shadow: 0px 0px 11px 1px rgba(194, 194, 194, 0.06);
      border-radius: 53px;
      padding: 17px;
      width: 100%;
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 400;
      font-size: 16px;
      line-height: 24px;
      letter-spacing: 0.02em;
      @media (max-width: 610px) {
        width: 100%;
      }
      @media (max-width: 425px) {
        line-height: 20px;
        font-size: 15px;
      }
      &::placeholder {
        color: #797979;
      }
      color: inherit;
    }
    span {
      position: absolute;
      top: -5px;
      right: 0px;
      width: 80px;
      height: 80px;
      @media (max-width: 610px) {
        right: 0px;
      }
      @media (max-width: 420px) {
        right: 0px;
      }
      @media (max-width: 320px) {
        right: 0px;
      }
    }
  }

  &__box {
    position: relative;
    width: 100%;
  }
  &__image {
    height: 400px;
    width: 100%;
    @media (max-width: 620px) {
      height: 350px;
    }
    @media (max-width: 400px) {
      height: 300px;
    }
    span {
      position: absolute;
      top: 35%;
      right: 300px;
      z-index: 2;
      img {
        @media (max-width: 620px) {
          right: -15px;
          width: 180px;
          height: 150px;
        }
        @media (max-width: 470px) {
          right: -65px;
          width: 150px;
          height: 120px;
        }
        @media (max-width: 400px) {
          right: -110px;
          width: 110px;
          height: 90px;
        }
      }
    }
    img {
      position: absolute;
      top: 35px;
      right: 50px;
      @media (max-width: 615px) {
        right: 10px;
        width: 300px;
        height: 350px;
      }
      @media (max-width: 470px) {
        right: 5px;
        width: 250px;
        height: 350px;
      }
      @media (max-width: 400px) {
        right: 5px;
        width: 220px;
        height: 300px;
      }
    }
  }
}
.cursor {
  cursor: pointer;
}
</style>
