<template>
  <header class="header">
    <div class="nav">
      <!-- logo -->
      <div class="logo">
        <img class="logo_img" src="../assets/img/logo.png" />
        <div class="logo_text">
          нии экологии
          <br />
          и природопользования
        </div>
      </div>

      <!-- service -->
      <div class="service">
        <ul>
          <li @click="scrollBlock('about-us')">О компании</li>
          <li @click="scrollBlock('services')">Услуги</li>
          <li @click="scrollBlock('completed-projects')">
            Выполненные проекты
          </li>
          <li @click="scrollBlock('input')">Контакты</li>
        </ul>
      </div>

      <!-- number -->
      <div class="number-section">
        <div class="number">
          <a class="number_tel" href="tel:+7(495)7997378">
            <p>+7(495)799-73-78</p></a
          >
          <a class="number_tel" href="tel:+7(909)0004960">
            <p>+7(909)000-49-60</p></a
          >
        </div>
        <button class="button" @click="scrollBlock('input')">
          Оставить заявку
        </button>
      </div>
      <img src="../assets/img/menu.svg" class="menubtn" @click="openMenu" />
    </div>
    <!-- home -->
    <div class="home-section">
      <h1>ГлавГосЭкспертиза</h1>
      <ul class="features">
        <li class="feature__item">
          Получение положительного экспертного заключения в сжатые сроки и по
          разумной цене
        </li>
        <li class="feature__item">
          Инжиниринговые и экспертные услуги более 12 лет
        </li>
        <li class="feature__item">Свыше 400 успешно реализованных проектов</li>
      </ul>
      <button class="button" @click="scrollBlock('input')">
        Оставить заявку
      </button>
    </div>
    <!-- menu -->
    <div class="menu" v-if="isMenu">
      <img
        src="../assets/img/close.svg"
        class="menu__close"
        @click="closeMenu"
      />
      <div class="menu__service">
        <ul>
          <li @click="scrollBlock('about-us')">О компании</li>
          <li @click="scrollBlock('services')">Услуги</li>
          <li @click="scrollBlock('completed-projects')">
            Выполненные проекты
          </li>
          <li @click="scrollBlock('input')">Контакты</li>
        </ul>
      </div>
      <button class="button" @click="scrollBlock('input')">
        Оставить заявку
      </button>
    </div>
  </header>
</template>

<script>
export default {
  name: "homeSectionComponent",
  data() {
    return {
      isMenu: false,
    };
  },
  methods: {
    scrollBlock(id) {
      this.closeMenu();
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
        block: "start",
      });
    },
    openMenu() {
      this.isMenu = true;
    },
    closeMenu() {
      if (!this.isMenu) return;
      this.isMenu = false;
    },
  },
  created() {
    document.addEventListener("keydown", (e) => {
      if (e.keyCode == 27) {
        this.isMenu = false;
      }
    });
    window.addEventListener("click", (e) => {
      const target = e.target;
      if (
        !target.closest(".menu") &&
        !target.closest(".menubtn") &&
        this.isMenu
      ) {
        this.isMenu = false;
      }
    });
    window.addEventListener("scroll", () => {
      const scrollPosition = document.documentElement.scrollTop;
      if (scrollPosition >= 120 && this.isMenu) {
        this.isMenu = false;
        // console.log(scrollPosition);
      }
    });
  },
};
</script>

<style lang="scss" scoped>
.nav {
  display: flex;
  justify-content: space-between;
  max-width: 1920px;
  align-items: center;
  padding-top: 40px;
  @media (max-width: 1200px) {
    padding-top: 20px;
  }
}
.menubtn {
  display: none;
  cursor: pointer;
  height: 40px;
  width: 40px;
  @media (max-width: 1200px) {
    display: flex;
    color: white;
  }
}
.menu {
  display: flex;
  flex-direction: column;
  position: fixed;
  justify-content: center;
  top: 0;
  right: 0;
  width: 310px;
  height: auto;
  background: #222423;
  z-index: 1;
  padding: 80px 20px 30px 20px;
  @media (max-width: 500px) {
    width: 100%;
  }
  &__close {
    color: #ffffff;
    cursor: pointer;
    position: absolute;
    top: 28px;
    right: 42px;
    font-size: 40px;
    width: 40px;
    height: 40px;
  }
  &__service {
    color: #ffffff;
    font-weight: 500;
    text-transform: uppercase;
    font-size: 20px;
    cursor: pointer;
    li {
      padding-top: 2px;
      padding-bottom: 2px;
    }
    li:hover {
      color: #ffffff7e;
    }
  }
  .button {
    margin-top: 20px;
    max-width: 310px;
    width: 100%;
    @media (max-width: 500px) {
      max-width: 500px;
    }
  }
}
.logo {
  display: flex;
  align-items: center;
  justify-content: center;
  &_img {
    max-height: 73px;
    @media (max-width: 1550px) {
      max-height: 63px;
    }
    @media (max-width: 1200px) {
      max-height: 56px;
    }
  }
  &_text {
    font-weight: 700;
    font-size: 20px;
    text-transform: uppercase;
    color: #ffffff;
    line-height: 24px;
    margin-left: 20px;
    @media (max-width: 1550px) {
      font-size: 16px;
      margin-left: 14px;
    }
    @media (max-width: 1200px) {
      margin-left: 10px;
      line-height: 22px;
    }
  }
}
.service {
  display: flex;
  color: #ffffff;
  font-weight: 500;
  text-transform: uppercase;
  font-size: 20px;
  @media (max-width: 1550px) {
    font-size: 16px;
  }
  @media (max-width: 1200px) {
    display: none;
  }
  ul {
    list-style: none;
    margin: 0;
    padding: 20px;
    @media (max-width: 1550px) {
      padding: 20px 10px;
    }
  }
  li {
    cursor: pointer;
    display: inline;
    margin: 16px;
    @media (max-width: 1550px) {
      margin: 16px 10px;
    }
  }
  li:hover {
    color: #ffffff7e;
  }
}
.number-section {
  display: flex;
  align-items: center;
  justify-content: center;
  @media (max-width: 1200px) {
    display: none;
  }
}
.number {
  padding-right: 25px;
  flex-direction: column;
  @media (max-width: 1550px) {
    padding-right: 18px;
  }
  &_tel {
    color: #ffffff;
    font-size: 20px;
    font-weight: 700;
    line-height: 20px;
    @media (max-width: 1550px) {
      font-size: 16px;
    }
  }
  &_tel:hover {
    color: #ffffff7e;
  }
}
.button {
  background-color: #44d370;
  color: #ffffff;
  font-size: 16px;
  border-radius: 10px;
  max-width: 200px;
  height: 60px;
  font-weight: 700;
  border: 0;
  @media (max-width: 1550px) {
    font-size: 12px;
    height: 50px;
    max-width: 160px;
  }
}
.home-section {
  max-width: 750px;
  min-height: 410px;
  margin-top: 104px;
  @media (max-width: 768px) {
    margin-top: 70px;
  }
  h1 {
    font-weight: 700;
    font-size: 76px;
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
  .features {
    list-style: none;
    li {
      position: relative;
      color: #ffffff;
      font-weight: 500;
      font-size: 32px;
      margin-top: 5px;
      line-height: 42px;
      @media (max-width: 1550px) {
        font-size: 28px;
      }
      @media (max-width: 768px) {
        line-height: normal;
      }
      &:first-child {
        margin-top: 18px;
      }
      &::before {
        content: "✓";
        display: inline-block;
        font-size: 40px;
        color: #44d370;
        @media (max-width: 1550px) {
          font-size: 36px;
        }
      }
    }
  }
  button {
    margin-top: 60px;
    @media (max-width: 500px) {
      margin-top: 30px;
    }
  }
}
</style>