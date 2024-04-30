<template>
  <div class="documents-section">
    <div class="documents-section__left">
      <div class="container">
        <h1 class="documents-section__title">Необходимая документация</h1>
        <div class="documents-section__text">
          <p>
            Успешное прохождение ГлавГосЭкспертизы предусматривает
            предоставление полного комплекта проектной и сопутствующей
            документации. В его состав входят:
          </p>
        </div>
        <ul class="documents-section__info">
          <li>Заявление на прохождение экспертизы</li>
          <li>Проект в полном составе</li>
          <li>Подтверждение правильности сметного расчета</li>
          <li>
            Информация о лицах и организациях, занимавшихся разработкой проекта
          </li>
          <li>Решение по объекту (при наличии)</li>
          <li>ТЗ на проведение инженерных изысканий и проектирование</li>
          <li>Экспертное заключение по инженерным изысканиям (при наличии)</li>
          <li>Акт осмотра объекта</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "documentsComponent",
};
</script>

<style lang="scss" scoped>
.documents-section {
  margin: 0;
  &__left {
    display: flex;
    flex-direction: column;
    width: 50%;
    background-color: #ffffff;
    opacity: 90%;
    @media (max-width: 1024px) {
      max-width: 1024;
      width: 100%;
    }
    .container {
      padding-top: 120px;
      padding-left: 142px;
      padding-bottom: 130px;
      @media (max-width: 1800px) {
        padding: 120px 40px 130px 40px;
      }
      @media (max-width: 1200px) {
        padding-top: 60px;
        padding-bottom: 60px;
      }
      @media (max-width: 768px) {
        padding: 60px 35px;
      }
      @media (max-width: 500px) {
        padding: 30px 20px;
      }
    }
  }
  &__title {
    font-weight: 700;
    font-size: 76px;
    line-height: 70px;
    color: #000000;
    max-width: 500px;
    @media (max-width: 1440px) {
      font-size: 66px;
    }
    @media (max-width: 1200px) {
      font-size: 56px;
      max-width: 1200px;
      line-height: 50px;
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
    max-width: 470px;
    padding-top: 62px;
    @media (max-width: 1024px) {
      padding-top: 40px;
      font-size: 18px;
      max-width: 1024px;
    }
    @media (max-width: 768px) {
      padding-top: 20px;
    }
  }
  &__info {
    max-width: 320px;
    padding-top: 47px;
    @media (max-width: 1024px) {
      max-width: 1024px;
    }
    @media (max-width: 768px) {
      padding-top: 30px;
    }
    @media (max-width: 500px) {
      padding-top: 10px;
    }
    li {
      font-weight: 500;
      font-size: 16px;
      line-height: 17.6px;
      color: #000000;
      padding: 5px 0;
      @media (max-width: 768px) {
        padding-top: 5px;
        font-size: 16px;
      }
    }
  }
}
</style>