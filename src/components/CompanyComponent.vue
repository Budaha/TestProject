<template>
  <div class="company-section">
    <h1 class="company-section-title">ГлавГосЭкспертиза</h1>
    <div class="company-section__block">
      <img class="company-section__img" src="../assets/img/Rectangle 24.png" />
      <div class="company-section__text">
        <p>
          НИИ «Экологии и Природопользования» предоставляет услугу сопровождения
          ГлавГосЭкспертизы. Участие наших специалистов в подготовке
          документации обеспечивает получение положительного экспертного
          заключения в сжатые сроки, с первого раза и по разумной цене.
        </p>
        <p>
          При необходимости выполняется разработка СТУ, что позволяет снизить
          стоимость объекта. Услуга предоставляется под ключ, то есть до
          получения разрешения на строительство. Бонусом становится возможность
          разработки экологической части проектной документации с нуля.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "companyComponent",
};
</script>

<style lang="scss" scoped>
.company-section {
  display: flex;
  flex-direction: column;
  &-title {
    font-weight: 700;
    font-size: 76px;
    line-height: 70px;
    color: #ffffff;
    @media (max-width: 1440px) {
      font-size: 66px;
    }
    @media (max-width: 768px) {
      font-size: 56px;
    }
    @media (max-width: 500px) {
      font-size: 36px;
    }
  }
  &__block {
    display: flex;
    padding-top: 60px;
    @media (max-width: 1200px) {
      display: flex;
      flex-direction: column;
    }
    @media (max-width: 768px) {
      padding-top: 40px;
    }
    @media (max-width: 500px) {
      padding-top: 20px;
    }
  }
  &__img {
    max-width: 808px;
    margin-right: 98px;
    @media (max-width: 1200px) {
      max-width: 1200px;
      margin: 0;
    }
  }
  &__text {
    margin-top: 41px;
    line-height: 21.6px;
    color: #ffffff;
    max-width: 570px;
    @media (max-width: 1200px) {
      max-width: 1200px;
      width: 100%;
    }
    p {
      &:first-child {
        padding-bottom: 24px;
      }
    }
  }
}
.company-section-img {
  img {
    margin-top: 60px;
  }
}
</style>