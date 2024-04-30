<template>
  <div class="footer-section">
    <div class="footer-section__grid">
      <!-- logo -->
      <div class="info">
        <div class="logo" @click="scrollBlock('home')">
          <img class="logo__img" src="../assets/img/logo.png" />
          <div class="logo__text">
            <p>
              нии экологии
              <br />
              и природопользования
            </p>
          </div>
        </div>
        <p class="confidentiality">Политика конфиденциальности</p>
      </div>
      <!-- service first -->
      <ul class="footer-section__service-first">
        <li @click="scrollBlock('about-us')">О компании</li>
        <li @click="scrollBlock('services')">Услуги</li>
        <li @click="scrollBlock('completed-projects')">Выполненные проекты</li>
        <li @click="scrollBlock('input')">Контакты</li>
      </ul>
      <!-- service-second -->
      <ul class="footer-section__service-second">
        <li>Государственная экологическая экспертиза</li>
        <li>Лицензия на отходы</li>
        <li>ГлавГосЭкспертиза</li>
        <li>Готовый бизнес</li>
      </ul>
      <!-- contacs -->
      <div class="footer-section__contacs">
        <a class="number_tel" href="tel:+7(495)7997378">
          <p>+7(495)799-73-78</p></a
        >
        <a class="number_tel" href="tel:+7(909)0004960">
          <p>+7(909)000-49-60</p></a
        >
        <p>г.Москва, ул.Большая Грузинская,д.30а,стр.1</p>
        <a href="mailto:info@prirodarf.expert">info@prirodarf.expert</a>
        <div class="icons">
          <a href="https://web.telegram.org/"
            ><img src="../assets/img/telegram.svg"
          /></a>
          <a href="https://web.whatsapp.com/"
            ><img src="../assets/img/whatsapp.svg"
          /></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "footerComponent",
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
.footer-section {
  &__grid {
    display: grid;
    grid-template-columns: 390px 360px 390px 400px;
    padding-top: 35px;
    @media (max-width: 1600px) {
      grid-template-columns: repeat(4, 1fr);
    }
    @media (max-width: 1440px) {
      padding-top: 0;
    }
    @media (max-width: 1024px) {
      grid-template-columns: repeat(3, 1fr);
    }
    @media (max-width: 768px) {
      display: flex;
      flex-direction: column;
    }
  }
  .info {
    align-items: center;
    .logo {
      display: flex;
      cursor: pointer;
      &__img {
        max-height: 64px;
        @media (max-width: 1024px) {
          max-height: 56px;
        }
      }
      &__text {
        p {
          font-weight: 700;
          font-size: 17px;
          text-transform: uppercase;
          color: #ffffff;
          line-height: 21px;
          margin-left: 20px;
          margin-top: 13px;
          @media (max-width: 1440px) {
            font-size: 16px;
            line-height: 24px;
          }
          @media (max-width: 1024px) {
            margin-left: 10px;
            font-size: 16px;
            line-height: 20px;
          }
        }
      }
    }
    .confidentiality {
      color: gray;
      font-weight: 500;
      text-decoration: underline;
      margin-top: 30px;
      font-size: 17px;
      cursor: pointer;
      @media (max-width: 1024px) {
        font-size: 15px;
      }
    }
  }
  &__service-first {
    color: #ffffff;
    font-weight: 700;
    padding-left: 60px;
    line-height: 38px;
    @media (max-width: 1440px) {
      font-size: 16px;
      line-height: 32px;
    }
    @media (max-width: 768px) {
      padding-left: 0;
    }
    li {
      cursor: pointer;
    }
    li:hover {
     color: #ffffff7e;
    }
  }
  &__service-second {
    color: #ffffff;
    font-weight: 700;
    line-height: 38px;
    @media (max-width: 1440px) {
      font-size: 16px;
      line-height: 32px;
    }
    @media (max-width: 768px) {
      padding-top: 20px;
    }
  }
  &__contacs {
    color: #ffffff;
    font-weight: 700;
    line-height: 38px;
    padding-left: 60px;
    @media (max-width: 1440px) {
      font-size: 16px;
      line-height: 32px;
    }
    @media (max-width: 1024px) {
      padding-left: 0;
      padding-top: 20px;
    }
    a {
      color: #ffffff;
    }
    a:hover {
     color: #ffffff7e;
    }
    .icons {
      display: flex;
      gap: 0 10px;
      img {
        width: 25px;
        height: 25px;
      }
    }
  }
}
</style>