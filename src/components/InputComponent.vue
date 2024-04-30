<template>
  <div class="input-home">
    <div class="input-section">
      <div class="input-section__info">
        <h1 class="input-section__title">Остались вопросы?</h1>
        <input
          class="input-name"
          v-model="inputPush.name"
          type="text"
          placeholder="Ваше имя"
        />
        <input
          class="input-number"
          v-model="inputPush.number"
          @input="test"
          placeholder="Ваш телефон"
        />
        <button class="button" @click="submitForm">Оставить заявку</button>
        <p class="text">
          Нажимая на кнопку, вы даёте согласие на
          <span>обработку персональных данных</span>
        </p>
      </div>
      <div class="input-section__contacts">
        <h3>Свяжитесь с нами</h3>
        <div class="number-section">
          <a class="number_tel" href="tel:+7(495)7997378">
            <p>+7(495)799-73-78</p></a
          >
          <a class="number_tel" href="tel:+7(909)0004960">
            <p>+7(909)000-49-60</p></a
          >
        </div>
        <a href="mailto:info@prirodarf.expert">info@prirodarf.expert</a>
        <div class="icons">
          <a href="https://web.telegram.org/"
            ><img src="../assets/img/telegram.svg"
          /></a>
          <a href="https://web.whatsapp.com/"
            ><img src="../assets/img/whatsapp.svg"
          /></a>
        </div>
        <div class="adress">
          <h3>Наш адрес</h3>
          <p>г.Москва, ул. Большая Грузинская, д. 30а, стр. 1</p>
        </div>
        <div class="time">
          <h3>Рабочие часы</h3>
          <p>Каждый день с 9:00 до 18:00</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "inputComponent",
  data() {
    return {
      inputPush: {
        name: "",
        number: "",
      },
    };
  },
  methods: {
    submitForm() {
      console.log({
        name: this.inputPush.name,
        number: this.inputPush.number,
      }) & alert("Выполнено!");
      (this.inputPush.name = ""),
      (this.inputPush.number = "");
    },
    test(e) {
      console.log(e.target.value)
      if(e.target.value === '+') {
        this.inputPush.number = ''
        return
      }
      const test = e.target.value
        const x = test.replace(/\D/g, '').match(/(\d{0,1})(\d{0,3})(\d{0,3})(\d{0,4})/)
        if (!x[2] && x[1] !== '') {
          this.inputPush.number = x[1] === '7' ? '+' + x[1] : '+' + '7' + x[1]
        } else {
            this.inputPush.number = !x[3] ? '+' + x[1] + x[2] : '+' + x[1] + '(' + x[2] + ') ' + x[3] + (x[4] ? '-' + x[4] : '')
        }
    }
  },
};
</script>

<style lang="scss" scoped>
.input-home {
  background: url(../assets/img/input.png);
  width: 95%;
}
.input-section {
  display: flex;
  gap: 0 53px;
  padding-bottom: 70px;
  justify-content: center;
  @media (max-width: 768px) {
    flex-direction: column;
    padding-bottom: 0;
  }
  &__info {
    background-color: #ffffff;
    width: 776px;
    height: 518px;
    margin-top: 77px;
    display: flex;
    flex-direction: column;
    @media (max-width: 1440px) {
      width: 650px;
      padding: 54px;
      justify-content: center;
    }
    @media (max-width: 768px) {
      width: 95%;
      height: 400px;
    }
  }
  &__title {
    font-weight: 700;
    font-size: 66px;
    padding-top: 95px;
    padding-left: 54px;
    line-height: 20px;
    @media (max-width: 1440px) {
      font-size: 56px;
      padding: 0;
    }
    @media (max-width: 1200px) {
      font-size: 46px;
    }
    @media (max-width: 1024px) {
      font-size: 36px;
      line-height: 30px;
    }
    @media (max-width: 865px) {
      font-size: 25px;
    }
  }
  input {
    width: 470px;
    border: 0;
    border-bottom: 2px solid #44d370;
    @media (max-width: 1440px) {
      width: 100%;
    }
  }
  .input-name {
    margin-top: 95px;
    margin-left: 50px;
    @media (max-width: 1440px) {
      margin: 0;
      margin-top: 65px;
    }
    @media (max-width: 1024px) {
      margin: 0;
      margin-top: 35px;
      font-size: 13px;
    }
  }
  .input-number {
    margin-top: 45px;
    margin-left: 50px;
    @media (max-width: 1440px) {
      margin: 0;
      margin-top: 25px;
    }
    @media (max-width: 1024px) {
      font-size: 13px;
    }
  }
  input[type="number"]::-webkit-inner-spin-button,
  input[type="number"]::-webkit-outer-spin-button {
    -webkit-appearance: none;
    margin: 0;
  }
  .button {
    margin-top: 39px;
    margin-left: 53px;
    height: 40px;
    width: 173px;
    font-size: 14px;
    @media (max-width: 1440px) {
      margin: 0;
      margin-top: 25px;
    }
  }
  .text {
    padding-top: 22px;
    padding-left: 54px;
    font-size: 17px;
    @media (max-width: 1440px) {
      padding: 0;
      margin-top: 25px;
    }
    @media (max-width: 1024px) {
      font-size: 15px;
    }
    span {
      text-decoration: underline;
      cursor: pointer;
    }
  }
  &__contacts {
    margin-top: 77px;
    background-color: #222423;
    height: 518px;
    width: 435px;
    display: flex;
    flex-direction: column;
    padding: 54px;
    @media (max-width: 768px) {
      width: 95%;
      margin-top: 35px;
      padding-bottom: 10px;
      height: 400px;
      margin-bottom: 77px;
    }
    h3 {
      font-weight: 700;
      font-size: 19px;
      color: #ffffff;
      @media (max-width: 1024px) {
        font-size: 16px;
      }
    }
    .number-section {
      display: flex;
      gap: 0 15px;
      padding-top: 23px;
      padding-bottom: 23px;
      @media (max-width: 1024px) {
        flex-direction: column;
        padding-top: 10px;
        padding-bottom: 10px;
      }
    }
    a {
      color: #ffffff;
      @media (max-width: 1024px) {
        font-size: 15px;
      }
    }
    a:hover {
     color: #ffffff7e;
    }
    .icons {
      display: flex;
      gap: 0 20px;
      padding-top: 20px;
      @media (max-width: 1024px) {
        padding-top: 10px;
      }
      img {
        width: 30px;
        height: 30px;
        @media (max-width: 1024px) {
          width: 20px;
          height: 20px;
        }
      }
    }
  }
  .adress {
    color: #ffffff;
    padding-top: 50px;
    @media (max-width: 1024px) {
      padding-top: 10px;
    }
    p {
      font-size: 17px;
      padding-top: 23px;
      @media (max-width: 1024px) {
        padding-top: 10px;
        font-size: 15px;
      }
    }
  }
  .time {
    color: #ffffff;
    padding-top: 42px;
    @media (max-width: 1024px) {
      padding-top: 10px;
    }
    p {
      font-size: 17px;
      padding-top: 23px;
      @media (max-width: 1024px) {
        padding-top: 10px;
        font-size: 15px;
      }
    }
  }
}
</style>