<template>
  <div class="other-services">
    <div class="other-services__text">
      <h1 class="other-services__title">Другие услуги</h1>
      <h1 class="other-services__info">Услуги</h1>
    </div>
    <div class="other-services__img">
      <div class="image">
        <img src="../assets/img/otherServ1.png" />
        <p>ГЭЭ-Государственная экологическая экспертиза</p>
      </div>
      <div class="image">
        <img src="../assets/img/otherServ2.png" />
        <p>ГГЭ-Глав гос.экспертиза</p>
      </div>
      <div class="image">
        <img src="../assets/img/otherServ3.png" />
        <p>ЭКОЗОС</p>
      </div>
      <div class="image">
        <img src="../assets/img/otherServ4.png" />
        <p>Комплексное проектирование обьектов размещения отходов</p>
      </div>
      <div class="image">
        <img src="../assets/img/otherServ5.png" />
        <p>Лицензния на утилизацию отходов</p>
      </div>
      <div class="image">
        <img src="../assets/img/otherServ6.png" />
        <p>Готовые компании</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "otherServicesComponent",
};
</script>

<style lang="scss" scoped>
.other-services {
  &__text {
    display: flex;
    @media (max-width: 768px) {
      gap: 0;
    }
  }
  &__title {
    font-weight: 700;
    font-size: 66px;
    line-height: 70px;
    color: #000000;
    padding-top: 65px;
    width: 30%;
    @media (max-width: 1455px) {
      padding-top: 50px;
      font-size: 56px;
      line-height: 50px;
      width: 40%;
    }
    @media (max-width: 768px) {
      width: 100%;
    }
    @media (max-width: 500px) {
      font-size: 36px;
    }
  }
  &__info {
    font-weight: 600;
    font-size: 275px;
    line-height: 0.75;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: #daf6e2;
    user-select: none;
    width: 70%;
    text-align: right;
    @media (max-width: 1455px) {
      font-size: 185px;
      width: 60%;
    }
    @media (max-width: 1200px) {
      font-size: 145px;
      padding-top: 10px;
    }
    @media (max-width: 1024px) {
      font-size: 115px;
      padding-top: 20px;
    }
    @media (max-width: 768px) {
      display: none;
    }
  }
  &__img {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 40px 40px;
    margin-top: 20px;
    @media (max-width: 1024px) {
      grid-template-columns: repeat(2, 1fr);
    }
    @media (max-width: 768px) {
      grid-template-columns: repeat(1, 1fr);
    }
    .image {
      position: relative;
      width: 100%;
      img {
        width: 500px;
        height: 350px;
        @media (max-width: 1200px) {
          height: 280px;
        }
      }
      p {
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        width: 100%;
        height: 50px;
        bottom: 0;
        max-width: 500px;
        color: #ffffff;
        font-weight: 700;
        opacity: 70%;
        background: #000000;
      }
    }
  }
}
</style>