<template>
  <div class="risks-section">
    <h1 class="risks-section__title">Риски самостоятельного прохождения ГГЭ</h1>
    <div class="risks-section__text">
      <div class="risks-section__text-left">
        <p>
          Успешное прохождение ГлавГосЭкспертизы – непростая задача даже для
          профессионалов. Дело в том, что реализация мероприятия имеет ярко
          выраженную специфику в виде крайне высоких требований со стороны
          контролирующего органа. Дополнительные сложности создает их постоянное
          ужесточение, которое происходит в течение последних нескольких лет.
        </p>
      </div>
      <div class="risks-section__text-right">
        <p>
          В результате для получения положительного заключения ГГЭ требуется не
          только правильное оформление и содержание проектной документации, но и
          учет последних корректировок, внесенных в нормативно-правовую базу. Не
          менее важную роль играют наработанные связи с сотрудниками
          ГлавГосЭкспертизы. Законодательство устанавливает предельный срок
          проверки на уровне 42 рабочих дней с возможностью продления при
          выявлении недочетов или ошибок. Поэтому для быстрого получения нужного
          заказчику результата необходима ежедневная и кропотливая работа
          непосредственно с персоналом ГГЭ.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "risksComponent",
};
</script>

<style lang="scss" scoped>
.risks-section {
  &__title {
    font-weight: 700;
    font-size: 76px;
    line-height: 70px;
    color: #000000;
    max-width: 770px;
    @media (max-width: 1440px) {
      font-size: 66px;
    }
    @media (max-width: 1200px) {
      font-size: 56px;
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
    display: flex;
    justify-content: space-between;
    padding-top: 60px;
    @media (max-width: 1200px) {
      padding-top: 40px;
      gap: 25px;
    }
    @media (max-width: 500px) {
      flex-direction: column;
      max-width: 500px;
      width: 100%;
    }
  }
  &__text-left {
    width: 50%;
    @media (max-width: 500px) {
      width: 100%;
    }
    p {
      max-width: 650px;
      font-weight: 500;
      font-size: 20px;
      line-height: 26px;
      color: #000000;
      @media (max-width: 768px) {
        font-size: 18px;
      }
    }
  }
  &__text-right {
    width: 50%;
    @media (max-width: 500px) {
      width: 100%;
    }
    p {
      max-width: 710px;
      font-weight: 500;
      font-size: 18px;
      line-height: 21.6px;
      color: #000000;
      @media (max-width: 768px) {
        font-size: 16px;
      }
    }
  }
}
</style>