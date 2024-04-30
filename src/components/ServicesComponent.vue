<template>
  <div class="services-section">
    <h1 class="services-section__title">Что входит в состав услуги?</h1>
    <div class="services-section__text">
      <p>
        Сопровождение ГГЭ представляет собой комплексную услугу, оказание
        которой предусматривает выполнение следующих мероприятий:
      </p>
    </div>
    <div class="services-section__info">
      <ul class="services-section__info-grid">
        <li>
          <img
            class="services-section__info-icons"
            src="../assets/img/servicesGrid1.png"
          /><br />
          Проверка имеющейся документации с точки зрения комплектности и
          содержания
        </li>
        <li>
          <img
            class="services-section__info-icons"
            src="../assets/img/servicesGrid2.png"
          /><br />
          Аудит проекта на соответствие действующему законодательству
        </li>
        <li>
          <img
            class="services-section__info-icons"
            src="../assets/img/servicesGrid3.png"
          /><br />
          Проверка разделов проекта по вопросам выполнения требованиям
          технических регламентов
        </li>
        <li>
          <img
            class="services-section__info-icons"
            src="../assets/img/servicesGrid4.png"
          /><br />
          При необходимости – разработка недостающих или несоответствующих
          законодательству разделов проекта
        </li>
        <li>
          <img
            class="services-section__info-icons"
            src="../assets/img/servicesGrid5.png"
          /><br />
          Получение положительного экспертного заключения и проверка внесения
          сведений о нем в официальную базу данных ГлавГосЭкспертизы.
        </li>
        <li>
          <img
            class="services-section__info-icons"
            src="../assets/img/servicesGrid6.png"
          /><br />
          Консультационное сопровождение экспертных мероприятий в виде
          оперативного предоставления поясняющих и дополнительных материалов
        </li>
        <li>
          <img
            class="services-section__info-icons"
            src="../assets/img/servicesGrid7.png"
          /><br />
          Подача комплекта документов в ГГЭ
        </li>
      </ul>
      <div class="services-section__info-img">
        <img src="../assets/img/Rectangle 28.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "servicesComponent",
};
</script>

<style lang="scss" scoped>
.services-section {
  &__title {
    font-weight: 700;
    font-size: 76px;
    line-height: 70px;
    color: #000000;
    @media (max-width: 1440px) {
      font-size: 66px;
    }
    @media (max-width: 768px) {
      font-size: 56px;
    }
    @media (max-width: 500px) {
      font-size: 36px;
      line-height: 40px;
    }
  }
  &__text {
    font-weight: 500;
    font-size: 18px;
    line-height: 21.6px;
    color: #000000;
    margin-top: 61px;
    max-width: 530px;
    @media (max-width: 1200px) {
      max-width: 1200px;
      width: 100%;
    }
    @media (max-width: 768px) {
      margin-top: 30px;
    }
    @media (max-width: 500px) {
      margin-top: 15px;
    }
  }
  &__info {
    display: flex;
    justify-content: space-between;
    @media (max-width: 1200px) {
      flex-direction: column;
      width: 100%;
    }
  }
  &__info-grid {
    display: grid;
    grid-template-columns: repeat(2, 300px);
    grid-auto-rows: 157px;
    padding-top: 50px;
    gap: 0 128px;
    @media (max-width: 1200px) {
      grid-template-columns: repeat(2, 1fr);
      width: 100%;
      gap: 0 100px;
    }
    @media (max-width: 768px) {
      gap: 65px 5px;
      text-align: center;
    }
    li {
      font-weight: 500;
      font-size: 16px;
      line-height: 17.6px;
      color: #000000;
    }
  }
  &__info-icons {
    padding-bottom: 21px;
  }
  &__info-img {
    padding-top: 50px;
    @media (max-width: 1200px) {
      display: none;
    }
  }
}
</style>