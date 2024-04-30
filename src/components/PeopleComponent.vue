<template>
  <div class="people-section">
    <h1 class="people-section__title">Наши сотрудники</h1>
    <div class="people-section__slider">
      <Carousel
        class="info"
        v-bind="settings"
        :breakpoints="breakpoints"
        :wrap-around="true"
      >
        <Slide :key="1">
          <div class="item">
            <img src="../assets/img/people1.png" />
            <p class="name">Иван Васильевич</p>
            <p>Специалист в области управления проектами</p>
            <p>Опыт в сфере проектного управления: 12 лет</p>
          </div>
        </Slide>
        <Slide :key="2">
          <div class="item">
            <img src="../assets/img/people2.png" />
            <p class="name">Анатолий Михайлович</p>
            <p>ГИП</p>
            <p>Опыт в сфере проектирования: 12 лет</p>
          </div>
        </Slide>
        <Slide :key="3">
          <div class="item">
            <img src="../assets/img/people3.png" />
            <p class="name">Алексей Сергеевич</p>
            <p>Директор по связям с общественностью</p>
            <p>Опыт общественных обсуждений 10 лет.</p>
          </div>
        </Slide>
        <Slide :key="4">
          <div class="item">
            <img src="../assets/img/people4.png" />
            <p class="name">Максим Олегович</p>
            <p>Специалист в работе с обьектами размещения отходов</p>
            <p>Опыт в сфере ОРО: более 15 лет</p>
          </div>
        </Slide>
        <template #addons>
          <Navigation />
        </template>
      </Carousel>
    </div>
  </div>
</template>

<script>
import { Carousel, Navigation, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";
export default {
  name: "peopleComponent",
  components: {
    Carousel,
    Slide,
    Navigation,
  },
  data() {
    return {
      settings: {
        itemsToShow: 1,
        snapAlign: "center",
      },
      breakpoints: {
        1440: {
          itemsToShow: 4,
          snapAlign: "start",
        },
        1024: {
          itemsToShow: 3,
          snapAlign: "start",
        },
        768: {
          itemsToShow: 2,
          snapAlign: "start",
        },
        375: {
          itemsToShow: 1,
          snapAlign: "start",
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.people-section {
  &__title {
    font-weight: 700;
    font-size: 66px;
    line-height: 70px;
    color: #ffffff;
    @media (max-width: 1200px) {
      font-size: 56px;
    }
    @media (max-width: 500px) {
      font-size: 36px;
    }
  }
  .carousel__slide {
    display: block;
  }
  &__slider {
    padding-top: 10px;
    @media (max-width: 500px) {
      padding-top: 0;
    }
    .item {
      margin: 0 20px;
      .name {
        font-size: 18px;
        margin-top: 25px;
        font-weight: 700;
        margin-bottom: 15px;
        @media (max-width: 1023px) {
          text-align: center;
        }
      }
      p {
        font-size: 16px;
        color: #ffffff;
        font-weight: 500;
        text-align: left;
        @media (max-width: 1023px) {
          text-align: center;
        }
        @media (max-width: 1200px) {
          line-height: 21px;
        }
      }
    }
  }
  .info {
    @media (max-width: 500px) {
      padding-top: 10px;
    }
    cursor: pointer;
    ::v-deep(.carousel__prev) {
      color: gray;
      border-radius: 50px;
      background: white;
      width: 60px;
      height: 60px;
      @media (max-width: 768px) {
        width: 45px;
        height: 45px;
        background: none;
        color: #ffffff;
        margin: 0 -15px;
      }
    }
    ::v-deep(.carousel__next) {
      color: gray;
      border-radius: 50px;
      background: white;
      width: 60px;
      height: 60px;
      @media (max-width: 768px) {
        width: 45px;
        height: 45px;
        background: none;
        color: #ffffff;
        margin: 0 -15px;
      }
    }
  }
}
</style>