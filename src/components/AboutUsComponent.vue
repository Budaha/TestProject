<template>
  <div class="about">
    <div class="about-us">
      <h2>Почему стоит работать с нами?</h2>
      <div class="about-us-text">
        <p>
          Мы — Научно-Исследовательский Институт «Экологии и Природопользования»
          – это команда увлеченных экологией специалистов, с высочайшим уровнем
          профессиональных знаний и компетенций. Головной офис нашей компании
          находится в центре Москвы, а опыт выполненных работ есть практически в
          каждом регионе нашей страны.
        </p>
        <p>
          На сегодня наши специалисты накопили уникальный опыт в работе с
          отходами, начиная от наработок специалистов «старой школы» УРО РАН,
          так и современные методы по проектированию и внедрению технологий
          рекультивации объектов размещения отходов.
        </p>
      </div>
    </div>
    <div class="about-img">
      <div class="img-item">
        <img src="../assets/img/Vector.png" />
        <h3 class="text-title">100% гарантия</h3>
        <p class="text-descr">
          Гаранитрованно проведем по все этапам получения лицензии
        </p>
      </div>
      <div class="img-item">
        <img src="../assets/img/Group 21.png" />
        <h3 class="text-title">снижение рисков проекта</h3>
        <p class="text-descr">Пользуясь нашим опытом вы минимизируете риски</p>
      </div>
      <div class="img-item">
        <img src="../assets/img/Group 22.png" />
        <h3 class="text-title">снижение капитальных затрат проекта</h3>
        <p class="text-descr">
          Быстрое и качественное прохождение всех этапов гарантированно снижает
          затраты
        </p>
      </div>
      <div class="img-item">
        <img src="../assets/img/Group.png" />
        <h3 class="text-title">повышение скорости реализвции проекта</h3>
        <p class="text-descr">
          Знаем все тонкости и нюансы, что позволяет быстро получить все
          необходимые документы
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "aboutUsComponent",
};
</script>

<style lang="scss" scoped>
.about {
  display: flex;
  padding-top: 165px;
  padding-bottom: 121px;
  @media (max-width: 1200px) {
    padding-top: 60px;
    padding-bottom: 60px;
  }
}
.about-us {
  background-image: url("/src//assets/img/Rectangle.png");
  background-position: 50%;
  width: 50%;
  padding-right: 140px;
  @media (max-width: 1200px) {
    width: 100%;
    padding-right: 0;
  }
  h2 {
    font-weight: 800;
    font-size: 76px;
    color: #000000;
    line-height: 70px;
    @media (max-width: 1440px) {
      font-size: 66px;
    }
    @media (max-width: 768px) {
      font-size: 56px;
      line-height: 60px;
    }
    @media (max-width: 500px) {
      font-size: 36px;
      line-height: 40px;
    }
  }
}
.about-us-text {
  margin-top: 60px;
  @media (max-width: 768px) {
    margin-top: 30px;
  }
  p {
    display: block;
    font-weight: 500;
    font-size: 20px;
    line-height: 26px;
    color: #000000;
    margin-top: 20px;
    @media (max-width: 500px) {
      font-size: 18px;
    }
  }
}
.about-img {
  width: 50%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0 30px;
  @media (max-width: 1200px) {
    padding-top: 40px;
    grid-template-columns: 1fr 1fr;
    width: 100%;
    gap: 30px;
  }
  @media (max-width: 768px) {
    grid-template-columns: 1fr;
    width: 100%;
  }
  .img-item {
    @media (max-width: 1200px) {
      text-align: center;
    }
  }
  .text-title {
    font-weight: 500;
    font-size: 18px;
    line-height: 21.6px;
    color: #000000;
    text-transform: uppercase;
    margin-top: 21px;
  }
  .text-descr {
    font-weight: 500;
    font-size: 16px;
    line-height: 17.6px;
    color: #000000;
    margin-top: 10px;
  }
}
</style>