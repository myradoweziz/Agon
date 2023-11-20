<script setup>
  import ButtonAll from './base/ButtonAll.vue'
  import BaseIcon from './BaseIcon.vue'
  import CrossPlan from './base/CrossPlan.vue'
</script>

<template>
  <div class="cross">
    <div class="cross__container">
      <div class="cross__btn">
        <button-all title="How It Work ?" ping-color radius-btn="48" height-btn="36" />
      </div>
      <div class="cross__title">
        Cross-border ordering has <br />
        never been easier
      </div>
      <div class="cross__views">
        <cross-plan
          icon="light"
          title="Start Plan"
          first-name="Choose any of"
          last-name="our packages"
          bg-color="#FFF3EA"
        />
        <div class="cross__arrow">
          <BaseIcon name="dashedArrow" />
        </div>
        <cross-plan
          icon="connect"
          title="Connect"
          first-name="Receive concepts"
          last-name=" In 24 hours"
          bg-color="#FDE2E4"
        />
        <div class="cross__arrow">
          <base-icon name="dashedArrow" />
        </div>
        <cross-plan icon="match" title="Match" first-name="Development" last-name="Stage" bg-color="#DBECE5" />
      </div>
      <div class="cross__circle-arrow">
        <base-icon name="dashedCircleArrow" />
      </div>
      <div>
        <div class="cross__review review_cross">
          <cross-plan
            icon="complete"
            title="Complete"
            first-name="After-release"
            last-name="Support"
            bg-color="#DBECE5"
          />
          <div class="review_cross__arrow">
            <base-icon name="dashedRevArrow" />
          </div>
          <cross-plan
            icon="review"
            title="Review"
            first-name="Project launch"
            last-name="and checkout"
            bg-color="#D1ECFD"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .cross {
    padding-bottom: 100px;
    @media (max-width: 479px) {
      padding-bottom: 30px;
    }
    &__container {
      max-width: 1240px;
      margin: 0 auto;
      overflow: hidden;
      padding: 0 10px;
    }
    &__title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 600;
      font-size: 50px;
      line-height: 60px;
      text-align: center;
      color: #101828;
      padding-bottom: 60px;
      @media (max-width: 706px) {
        font-size: 45px;
        padding-bottom: 20px;
      }
      @media (max-width: 406px) {
        font-size: 30px;
        line-height: 40px;
      }
      @media (max-width: 320px) {
        font-size: 25px;
        br {
          display: none;
        }
      }
    }
    &__btn {
      display: flex;
      justify-content: center;
      padding-bottom: 20px;
    }
    &__views {
      display: flex;
      gap: 50px;
      align-items: center;
      padding-bottom: 60px;
      @media (max-width: 1293px) {
        flex-wrap: wrap;
      }
      @media (max-width: 756px) {
        flex-direction: column;
        padding-bottom: 30px;
      }
    }
    &__image {
    }
    &__arrow {
      @media (max-width: 750px) {
        margin: 0 auto;
        transform: rotate(100deg);
      }
    }
    &__circle-arrow {
      display: flex;
      justify-content: flex-end;
      padding-right: 50px;
      @media (max-width: 757px) {
        justify-content: center;
        padding-right: 0px;
        padding-bottom: 30px;
        transform: rotate(-50deg);
      }
    }
    &__review {
      margin-top: 0;
      margin-bottom: 0;
      margin-right: 20px;
      margin-left: 250px;
      @media (max-width: 1268px) {
        margin-left: 0;
        margin-right: 0;
      }
    }
  }

  .review_cross {
    display: flex;
    align-items: center;
    gap: 10px;
    @media (max-width: 1000px) {
      flex-wrap: wrap;
      gap: 50px;
    }
    @media (max-width: 750px) {
      flex-direction: column;
    }
    &__body {
      &:nth-child(3) {
        margin: 0px 120px 0 20px;
        padding: 45px 90px;
        background: #d1ecfd;
        @media (max-width: 1266px) {
          margin: 0;
        }
      }
    }
    &__image {
    }
    &__title {
      padding-top: 23px;
      padding-bottom: 30px;
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 500;
      font-size: 32px;
      line-height: 26px;
      text-align: center;
      color: #1e2534;
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
    &__arrow {
      @media (max-width: 750px) {
        transform: rotate(280deg);
      }
    }
  }
</style>
