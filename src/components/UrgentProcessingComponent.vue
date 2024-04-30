<template>
  <div class="urgent-section">
    <div class="urgent-section__block">
      <h1 class="urgent-section__title">Срочное оформление</h1>
      <div class="urgent-section__text">
        <span>Все условия и гарантии закреплены договором</span>
        <h2>1 месяц</h2>
      </div>
      <button class="button" @click="scrollBlock('input')">
        Оставить заявку
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "urgentProcessingComponent",
  methods: {
    scrollBlock(id) {
      console.log(id);
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
        block: "start",
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.urgent-section {
  background: url("../assets/img/Urgent.png");
  max-width: 1620px;
  width: 95%;
  min-height: 487px;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  @media (max-width: 1024px) {
    min-height: 400px;
  }
  @media (max-width: 768px) {
    background: none;
    min-height: 240px;
  }
  &__block {
    display: flex;
    flex-direction: column;
    float: right;
    padding-top: 7%;
    padding-right: 26%;
    @media (max-width: 1200px) {
      padding-top: 10%;
      padding-right: 15%;
      @media (max-width: 768px) {
        align-items: center;
        float: none;
        padding-top: 0;
        padding-right: 0;
      }
    }
  }
  &__title {
    font-weight: 700;
    font-size: 42px;
    line-height: 46.2px;
    color: #000000;
    @media (max-width: 500px) {
      font-size: 36px;
    }
  }
  &__text {
    margin-top: 30px;
    span {
      font-weight: 500;
      font-size: 20px;
      line-height: 26px;
      color: #000000;
      @media (max-width: 500px) {
        font-size: 18px;
      }
    }
    h2 {
      font-weight: 500;
      font-size: 20px;
      line-height: 26px;
      color: #000000;
      margin-top: 8px;
      @media (max-width: 500px) {
        font-size: 18px;
      }
    }
  }
  .button {
    margin-top: 60px;
    @media (max-width: 1250px) {
      margin-top: 20px;
    }
  }
}
</style>