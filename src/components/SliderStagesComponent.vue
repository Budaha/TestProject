<template>
  <div class="stages-section">
    <h1 class="stages-section__title">Этапы получения</h1>
    <!-- slide 1 -->
    <Carousel class="first" :items-to-show="1" :wrap-around="true">
      <Slide :key="1">
        <div class="stages-section__content">
          <div class="stages-section__img">
            <img src="../assets/img/sliderStages.png" />
          </div>
          <div class="stages-section__text">
            <h1>Сбор исходных данных</h1>
            <p>
              Предполагает получение информации как от заказчика услуги, так и
              органов власти - муниципальных и государственных. В том числе -
              технические условия, планы застройки, данные Федеральных и
              региональных целевых программ, другие подобные сведения.
            </p>
          </div>
        </div>
      </Slide>
      <!-- slide 2 -->
      <Slide :key="2">
        <div class="stages-section__content">
          <div class="stages-section__img">
            <img src="../assets/img/sliderStages.png" />
          </div>
          <div class="stages-section__text">
            <h1>Сбор исходных данных</h1>
            <p>
              Предполагает получение информации как от заказчика услуги, так и
              органов власти - муниципальных и государственных. В том числе -
              технические условия, планы застройки, данные Федеральных и
              региональных целевых программ, другие подобные сведения.
            </p>
          </div>
        </div>
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
    <h1 class="stages-section__title-project" id="completed-projects">
      Выполненные проекты
    </h1>
    <Carousel
      class="second"
      v-bind="settings"
      :breakpoints="breakpoints"
      :wrap-around="true"
    >
      <Slide :key="1">
        <div class="carousel__item">
          <img src="../assets/img/sliderStages2.png" />
          <p>ООО "Априт"</p>
        </div>
      </Slide>
      <Slide :key="2">
        <div class="carousel__item">
          <img src="../assets/img/sliderStages3.png" />
          <p>АО "Миратэкс-Групп"</p>
        </div>
      </Slide>
      <Slide :key="3">
        <div class="carousel__item">
          <img src="../assets/img/sliderStages1.png" />
          <p>АО "Тулачермет"</p>
        </div>
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
  </div>
</template>
<script>
import { Carousel, Navigation, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";
export default {
  name: "sliderStagesComponent",
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
.stages-section {
  ::v-deep(.carousel) {
    padding: 0;
    text-align: left;
  }
  &__title {
    font-weight: 700;
    font-size: 66px;
    line-height: 70px;
    color: #ffffff;
    margin-top: 25px;
    @media (max-width: 1440px) {
      font-size: 56px;
    }
    @media (max-width: 1440px) {
      margin-top: 0;
    }
    @media (max-width: 500px) {
      font-size: 36px;
    }
  }
  &__content {
    display: flex;
    cursor: pointer;
    @media (max-width: 768px) {
      flex-direction: column;
      align-items: center;
    }
  }
  &__img {
    margin-top: 50px;
    width: 50%;
    @media (max-width: 768px) {
      width: 70%;
    }
  }
  &__text {
    width: 50%;
    @media (max-width: 768px) {
      width: 100%;
    }
    h1 {
      font-weight: 700;
      font-size: 81px;
      padding-top: 52px;
      padding-left: 20px;
      line-height: 70px;
      color: #ffffff;
      @media (max-width: 1440px) {
        font-size: 66px;
      }
      @media (max-width: 1200px) {
        font-size: 56px;
        @media (max-width: 500px) {
          font-size: 36px;
          padding-top: 20px;
          line-height: 40px;
        }
      }
    }
    p {
      font-weight: 500;
      font-size: 17px;
      line-height: 21.6px;
      color: #ffffff;
      padding-left: 21px;
      padding-top: 23px;
      @media (max-width: 500px) {
        padding-top: 10px;
      }
    }
  }
  &__title-project {
    font-weight: 700;
    font-size: 66px;
    line-height: 70px;
    color: #ffffff;
    margin-top: 250px;
    padding-bottom: 55px;
    @media (max-width: 1200px) {
      font-size: 56px;
      margin-top: 100px;
    }
    @media (max-width: 500px) {
      margin-top: 50px;
    }
    @media (max-width: 500px) {
      font-size: 36px;
      line-height: 40px;
    }
  }
  .carousel__item {
    margin: 0 20px;
    position: relative;

    img {
      width: 100%;
      height: 350px;
      object-fit: cover;
      object-position: 50% 50%;
      @media (max-width: 1200px) {
        height: 250px;
      }
      @media (max-width: 768px) {
        height: 350px;
      }
      @media (max-width: 500px) {
        height: 250px;
      }
    }
    p {
      display: flex;
      justify-content: center;
      align-items: center;
      position: absolute;
      width: 100%;
      color: #ffffff;
      bottom: 0;
      font-weight: 700;
      background: #000000;
      opacity: 70%;
      height: 50px;
      width: 100%;
    }
  }
  .first {
    ::v-deep(.carousel__prev) {
      color: #ffffff;
      @media (max-width: 500px) {
        margin: 0 -15px;
      }
    }
    ::v-deep(.carousel__next) {
      color: #ffffff;
      @media (max-width: 500px) {
        margin: 0 -15px;
      }
    }
  }
  .second {
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
      @media (max-width: 500px) {
        background: none;
        color: #ffffff;
        width: 30px;
        height: 30px;
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
      @media (max-width: 500px) {
        width: 30px;
        height: 30px;
      }
    }
  }
}
</style>