<template>
  <div class="definition-section">
    <h1 class="definition-section__title">Определение</h1>
    <div class="definition-section__text">
      <p>
        ГлавГосЭкспертиза представляет собой федеральный надзорный орган,
        который подчиняется Минстрою и занимается государственной экспертизой
        проектов строительства и реконструкции объектов, отнесенных к технически
        сложным и крупным. К числу таковых относятся:
      </p>
    </div>
    <ul class="definition-section__grid">
      <li>федеральные дороги</li>
      <li>объекты культурного наследия</li>
      <li>
        объекты, возведение которых осуществляется на территории двух или
        большего числа регионов России
      </li>
      <li>стройки, которые финансируются из федерального бюджета</li>
      <li>
        особо опасные, уникальные или технически сложные здания и сооружения
      </li>
      <li>
        объекты, данные о которых имеют отношение к<br />
        государственной тайне
      </li>
    </ul>
    <div class="definition-section__img">
      <img src="../assets/img/Rectangle 4.png" />
    </div>
  </div>
</template>

<script>
export default {
  name: "definitionComponent",
};
</script>

<style lang="scss" scoped>
.definition-section {
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
    }
  }
  &__text {
    font-weight: 500;
    font-size: 18px;
    line-height: 21.6px;
    color: #000000;
    max-width: 660px;
    margin-top: 62px;
    @media (max-width: 1200px) {
      max-width: 1200px;
      width: 100%;
    }
    @media (max-width: 768px) {
      margin-top: 40px;
    }
    @media (max-width: 500px) {
      margin-top: 20px;
    }
  }
  &__grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 48px;
    padding: 42px 28px;
    @media (max-width: 1200px) {
      grid-template-columns: repeat(2, 1fr);
      width: 100%;
      gap: 30px;
    }
    @media (max-width: 768px) {
      gap: 20 0px;
    }
    @media (max-width: 500px) {
      gap: 10 0px;
    }
    li {
      font-size: 16px;
      font-weight: 500;
      line-height: 17.6px;
      color: #000000;
      list-style: disc;
    }
  }
  &__img {
    padding-top: 20px;
    @media (max-width: 768px) {
      padding-top: 0;
    }
  }
}
</style>