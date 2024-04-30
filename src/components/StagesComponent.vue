<template>
  <div class="stages-section">
    <h1 class="stages-section__title">Этапы предоставления услуги ГГЭ</h1>
    <div class="stages-section__text">
      <p>
        Наша компания предоставляет инжиниринговые и экспертные услуги более 12
        лет. Это позволило разработать простую и эффективную схему
        сотрудничества с клиентами, многократно доказавшую эффективность на
        практике. Она предусматривает выполнение следующих работ:
      </p>
    </div>
    <ul class="stages-section__grid">
      <li>
        <h3>01</h3>
        <div class="underline" />
        <p>
          Прием заявки на оказание услуги. Сбор исходной информации. Первичная
          консультация.
        </p>
      </li>
      <li>
        <h3>02</h3>
        <div class="underline" />
        <p>
          Согласование условий сотрудничества – сроков, стоимости, обязательств
          каждой из сторон.
        </p>
      </li>
      <li>
        <h3>03</h3>
        <div class="underline" />
        <p>Подготовка и заключение договора.</p>
      </li>
      <li>
        <h3>04</h3>
        <div class="underline" />
        <p>Получение от заказчика и аудит проектной документации.</p>
      </li>
      <li>
        <h3>05</h3>
        <div class="underline" />
        <p>Подготовка недостающих документов и комплектование проекта.</p>
      </li>
      <li>
        <h3>06</h3>
        <div class="underline" />
        <p>
          Оформление заявления на проведение ГГЭ направление проекта на
          экспертизу.
        </p>
      </li>
      <li>
        <h3>07</h3>
        <div class="underline" />
        <p>Консультационное сопровождение проверки проекта.</p>
      </li>
      <li>
        <h3>08</h3>
        <div class="underline" />
        <p>
          Получение положительного экспертного заключения ГГЭ и передача его
          клиенту.
        </p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "stagesComponent",
};
</script>

<style lang="scss" scoped>
.stages-section {
  &__title {
    font-weight: 700;
    font-size: 76px;
    line-height: 70px;
    color: #ffffff;
    max-width: 800px;
    padding-top: 120px;
    @media (max-width: 1440px) {
      font-size: 66px;
    }
    @media (max-width: 768px) {
      font-size: 56px;
      line-height: 60px;
      padding-top: 60px;
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
    color: #ffffff;
    max-width: 640px;
    padding-top: 61px;
    @media (max-width: 1200px) {
      max-width: 1200px;
      width: 100%;
    }
    @media (max-width: 768px) {
      padding-top: 30px;
    }
  }
  &__grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    padding-top: 51px;
    gap: 42px 102px;
    @media (max-width: 1440px) {
      gap: 42px 15px;
    }
    @media (max-width: 1200px) {
      grid-template-columns: repeat(3, 1fr);
    }
    @media (max-width: 768px) {
      grid-template-columns: repeat(2, 1fr);
      padding-top: 30px;
    }
    li {
      display: flex;
      flex-direction: column;
    }
    h3 {
      font-weight: 500;
      font-size: 60px;
      line-height: 72px;
      color: #ffffff;
    }
    .underline {
      height: 1px;
      width: 70px;
      background: #44d370;
      margin-top: 5px;
    }
    p {
      font-weight: 500;
      font-size: 16px;
      line-height: 17.6px;
      color: #ffffff;
      padding-top: 21px;
    }
  }
}
</style>