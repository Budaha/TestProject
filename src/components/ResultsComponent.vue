<template>
  <div class="results-section">
    <h1 class="results-section__title">
      Результат и плюсы обращения в НИИ «Экологии и Природопользования»
    </h1>
    <div class="results-section__text">
      <p>
        Наша экспертная компания обладает всем необходимым для успешного и
        быстрого прохождения ГлавГосЭкспертизы. За плечами специалистов НИИ 12
        успешных лет работы и свыше 400 реализованных проектов. Безупречную
        деловую репутацию института подтверждают многочисленные отзывы клиентов.
        Обращение к нам — это простой, быстрый и доступный способ получить
        положительное экспертное заключение ГГЭ.
      </p>
      <p class="par">
        Другими немаловажными достоинствами предлагаемого сотрудничества
        выступают:
      </p>
    </div>
    <div class="results-section__grid">
      <div class="element">
        <img src="../assets/img/resultsGrid1.png" /><br />
        <p>
          Прозрачная ценовая политика. Стоимость услуги фиксируется на этапе
          переговоров и заключения договора, после чего является твердой и не
          меняется в процессе выполнения работ.
        </p>
      </div>
      <div class="element">
        <img src="../assets/img/resultsGrid2.png" /><br />
        <p>
          Сжатые сроки прохождения экспертизы. Что особенно актуально, учитывая
          специфику проведения ГГЭ, которая нередко очень сильно затягивается.
        </p>
      </div>
      <div class="element">
        <img src="../assets/img/resultsGrid3.png" /><br />
        <p>
          Гарантия получения положительного заключения экспертизы. Достигается
          предварительным аудитом проектной документации и исправлением всех
          возможных неточностей, недочетов или некомплектности.
        </p>
      </div>
      <div class="element">
        <img src="../assets/img/resultsGrid4.png" /><br />
        <p>
          Индивидуальный подход к заказчикам. Предусматривает предоставление
          постоянным и крупным клиентам дополнительных скидок и преференций.
        </p>
      </div>
    </div>
    <p class="results-section__text-info">
      При желании заказчика готовы заключить долгосрочный договор на оказание
      экспертных и инжиниринговых услуг на персональных условиях. Докажем
      профессионализм наших специалистов и качество сервиса на деле.
    </p>
  </div>
</template>

<script>
export default {
  name: "resultsComponent",
};
</script>

<style lang="scss" scoped>
.results-section {
  &__title {
    font-weight: 700;
    font-size: 76px;
    line-height: 70px;
    color: #ffffff;
    max-width: 940px;
    @media (max-width: 1440px) {
      font-size: 66px;
    }
    @media (max-width: 1200px) {
      font-size: 54px;
    }
    @media (max-width: 768px) {
      line-height: 60px;
    }
    @media (max-width: 500px) {
      font-size: 36px;
      line-height: 40px;
    }
  }
  &__text {
    margin-top: 64px;
    @media (max-width: 1200px) {
      margin-top: 40px;
    }
    p {
      font-weight: 500;
      font-size: 18px;
      line-height: 21.6px;
      color: #ffffff;
      max-width: 620px;
      @media (max-width: 1200px) {
        max-width: 1200px;
        width: 100%;
      }
    }
    .par {
      margin-top: 21px;
      max-width: 630px;
    }
  }
  &__grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    margin-top: 50px;
    @media (max-width: 768px) {
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
      margin-top: 35px;
    }
    @media (max-width: 500px) {
      grid-template-columns: repeat(1, 1fr);
      gap: 15px;
      margin-top: 15px;
    }
    p {
      font-weight: 500;
      font-size: 16px;
      line-height: 19px;
      color: #ffffff;
      margin-top: 20px;
      max-width: 350px;
    }
    .element {
      &:not(:first-child) {
        border-left: 1px solid #d9d9d9;
        max-width: 400px;
        padding-left: 30px;
        @media (max-width: 768px) {
          border-left: none;
          padding-left: 0;
        }
      }
      @media (max-width: 768px) {
        border-left: none;
        border-bottom: 1px solid #d9d9d9;
        padding-bottom: 20px;
      }
    }
  }
  &__text-info {
    font-weight: 500;
    font-size: 18px;
    line-height: 21.6px;
    color: #ffffff;
    max-width: 600px;
    margin-top: 38px;
    @media (max-width: 500px) {
      margin-top: 38px;
    }
  }
}
</style>