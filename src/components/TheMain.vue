<script setup>
  import ButtonAll from './base/ButtonAll.vue'
  import BaseIcon from './BaseIcon.vue'

  const mainBannerViewCounts = [
    { icon: 'settings', count: '+12k', title: 'Projects done' },
    { icon: 'customer', count: '68k', title: 'Custommers' }
  ]
</script>
<template>
  <div class="watch">
    <div class="watch__contianer">
      <div class="watch__box">
        <div class="watch__content">
          <div class="watch__sub-title">Exclusive Smart Watch</div>
          <div class="watch__title">Let go of the Challenge See yourself better</div>
          <div class="watch__description">
            Connect your conversations with the tools and services that you use to get the job done. With over 1,500
            apps and a robust API
          </div>
          <div class="watch__btn-work">
            <button-all title="Get Started" primary-btn icon-name="arrowRight" radiusBtn="4" />
            <div class="watch__work">
              <button-all title="How it works" icon-name="arrowRight" />
            </div>
          </div>
          <div class="counts">
            <div v-for="(item, index) in mainBannerViewCounts" :key="index" class="watch__counts">
              <base-icon :name="item.icon" />
              <div class="watch__count-num">
                <span>{{ item.count }}</span>
                <p>{{ item.title }}</p>
              </div>
            </div>
          </div>
        </div>
        <div class="watch__image">
          <div class="watch__image__circle"></div>
          <div class="watch__image-smart">
            <img src="../assets/img/smat-watch.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .watch {
    padding-bottom: 100px;
    @media (max-width: 479px) {
      padding-bottom: 30px;
    }
    &__contianer {
      max-width: 1240px;
      margin: 0 auto;
      padding: 0 10px;
    }
    &__box {
      display: flex;
      justify-content: space-around;
      flex: 0 0 50%;
      width: 100%;
      @media (max-width: 972px) {
        flex-direction: column-reverse;
        flex-wrap: wrap;
        gap: 120px;
      }
    }
    &__content {
      width: 100%;
      @media (max-width: 972px) {
        text-align: center;
      }
    }
    &__sub-title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      font-size: 25px;
      line-height: 26px;
      color: #98a2b3;
      padding-bottom: 28px;
      @media (max-width: 972px) {
        padding-bottom: 10px;
        font-size: 24px;
      }
    }
    &__title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      font-size: 50px;
      line-height: 60px;
      color: #101828;
      padding-bottom: 28px;
      @media (max-width: 1181px) {
        line-height: 50px;
        font-size: 40px;
        padding-bottom: 10px;
      }
      @media (max-width: 972px) {
        font-size: 35px;
        line-height: 43px;
      }
      @media (max-width: 350px) {
        font-size: 35px;
      }
    }
    &__description {
      font-family: 'Merriweather';
      font-style: normal;
      font-weight: 400;
      font-size: 16px;
      line-height: 26px;
      letter-spacing: 0.045em;
      color: #475467;
      padding-bottom: 28px;
      @media (max-width: 972px) {
        font-size: 13px;
      }
    }
    &__btn-work {
      display: flex;
      gap: 28px;
      padding-bottom: 28px;
      @media (max-width: 972px) {
        justify-content: center;
      }
      @media (max-width: 450px) {
        flex-wrap: wrap;
        flex-direction: column;
        gap: 20px;
        button {
          width: 100%;
          p {
            flex: 1 1 auto;
          }
        }
      }
    }
    &__work {
    }
    &__counts {
      display: flex;
      align-items: center;
      gap: 10px;
      @media (max-width: 470px) {
        gap: 40px;
      }
    }
    &__count-num {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      line-height: 26px;
      padding-top: 20px;
      color: #66728b;
      span {
        font-size: 30px;
        color: #101828;
        @media (max-width: 470px) {
          font-size: 25px;
        }
      }
    }
    &__count {
      display: flex;
      gap: 10px;
      @media (max-width: 470px) {
        gap: 40px;
      }
    }
    &__num-count {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      display: flex;
      flex-direction: column;
      gap: 20px;
      padding-top: 20px;
      line-height: 9px;
      color: #66728b;
      span {
        font-size: 30px;
        color: #101828;
        padding-bottom: 5px;
        @media (max-width: 470px) {
          font-size: 25px;
        }
      }
    }
    &__image {
      position: relative;
      width: 100%;
      &::after {
        content: '';
        background-image: url(../assets/img/grafik.png);
        position: absolute;
        bottom: -70px;
        right: 10px;
        width: 200px;
        height: 200px;
        @media (max-width: 972px) {
          bottom: -110px;
          right: 250px;
        }
        @media (max-width: 768px) {
          bottom: -120px;
          right: 150px;
        }
        @media (max-width: 320px) {
          width: 164px;
          height: 130px;
          bottom: -50px;
          right: 5px;
        }
      }
      &::before {
        content: '';
        position: absolute;
        background-image: url(../assets/img/Ellipse3.png);
        bottom: -35px;
        left: 220px;
        width: 46px;
        height: 46px;
        @media (max-width: 972px) {
          bottom: -45px;
          left: 290px;
        }
        @media (max-width: 768px) {
          left: 220px;
        }
        @media (max-width: 320px) {
          left: 0px;
        }
      }
    }
    &__image__circle {
      position: absolute;
      width: 69px;
      height: 69px;
      &::before {
        content: '';
        background-image: url(../assets/img/Ellipse1.png);
        position: absolute;
        top: 60px;
        left: 50px;
        width: 69px;
        height: 69px;
        @media (max-width: 972px) {
          right: -210px;
          left: auto;
        }
        @media (max-width: 768px) {
          right: -170px;
        }
        @media (max-width: 320px) {
          top: 10px;
          right: 0px;
        }
      }
    }
    &__image-smart {
      img {
        position: absolute;
        top: 50px;
        right: 0;
        max-width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center;
        @media (max-width: 972px) {
          right: auto;
          left: 33%;
        }
        @media (max-width: 320px) {
          left: 0;
        }
      }
      &::after {
        content: '';
        position: absolute;
        background-image: url(../assets/img/Ellipse2.png);
        top: 0px;
        right: 30px;
        width: 46px;
        height: 46px;
        @media (max-width: 972px) {
          left: 55%;
          top: -10px;
          right: auto;
        }
        @media (max-width: 768px) {
          left: 59%;
        }
        @media (max-width: 320px) {
          left: 68%;
        }
      }
      @media (max-width: 972px) {
        height: 300px;
      }
    }
  }

  .counts {
    display: flex;
    align-items: center;
    gap: 50px;
    @media (max-width: 972px) {
      justify-content: center;
    }
    @media (max-width: 470px) {
      flex-wrap: wrap;
    }
  }
  .ellipse_1 {
  }
</style>
