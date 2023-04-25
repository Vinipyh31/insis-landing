<template>
  <footer>
    <div class="content">
      <div class="row">
        <div class="column">
          <span class="any-questions-title">Остались<br />вопросы?</span>
          <span class="leave-a-request">Оставляй заявку</span>
          <div class="arrow-container">
            <img
              src="@/assets/images/footer-arrow.svg"
              alt="arrow"
              class="arrow"
            />
          </div>
        </div>
        <div class="column">
          <span class="input-title">Объясняем понятно, решаем быстро</span>
          <div class="input-container">
            <input
              placeholder="+7 (___) ___-__-__"
              v-bind:value="phoneInput"
              maxlength="18"
              type="tel"
              @input="onPhoneChange"
            />
            <button class="call-me-btn">Позвоните мне</button>
          </div>
          <span class="agreement"
            >Нажимая на кнопку «Оставить заявку», вы даёте согласие на обработку
            персональных данных</span
          >
        </div>
      </div>
      <div class="horizontal-line"></div>
      <div class="row">
        <div class="column">
          <img
            class="logo"
            src="@/assets/images/white-logo.svg"
            alt="white-logo"
          />
          <span class="years">2007-2022 год</span>
        </div>
        <div class="column socials-column">
          <span class="socials-title">Мы в соц. сетях:</span>
          <div class="socials">
            <img class="socials__item" src="@/assets/images/vk.svg" alt="vk" />
            <img
              class="socials__item"
              src="@/assets/images/youtube.svg"
              alt="youtube"
            />
          </div>
        </div>
        <div class="column">
          <a href="tel:+88002506060" class="phone-number">8-800-250-60-60</a>
          <a href="mailto:info@profintel.ru" class="email">info@profintel.ru</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script >
export default {
  name: 'FooterSection',
  data: () => {
    return {
      phoneInput: '',
    }
  },
  methods: {
    onPhoneChange(event) {
      if (event.inputType === 'insertText') {
        if (this.phoneInput.slice(0, 4) !== '+7 (') {
          this.phoneInput = '+7 ('
        }
        if (this.phoneInput.length === 18) {
          return
        }

        this.phoneInput += event.data

        if (this.phoneInput.length === 7) {
          this.phoneInput += ') '
        }

        if (this.phoneInput.length === 12) {
          this.phoneInput += '-'
        }
        if (this.phoneInput.length === 15) {
          this.phoneInput += '-'
        }
      }
      if (event.inputType === 'deleteContentBackward') {
        this.phoneInput = this.phoneInput.slice(0, this.phoneInput.length - 1)
      }
    },
  },
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

footer {
  background-color: $green;
  padding-top: 80px;
  padding-bottom: 98px;
  color: white;
  font-weight: 400;

  .socials {
    margin-top: 5px;
    display: flex;
    justify-content: space-between;

    &-title {
      font-size: 12px;
      line-height: 31px;
    }

    &__item {
      cursor: pointer;
    }
  }

  .arrow-container {
    padding-left: 136px;
  }

  a {
    color: white;
    text-decoration: none;
  }
}

.input {
  &-title {
    font-size: 24px;
    line-height: 36px;
    margin-bottom: 40px;
  }

  &-container {
    display: flex;
    height: 77px;

    input {
      border: none;
      margin-right: -107px;
      border-radius: 50px;
      width: 410px;
      font-weight: 400;
      font-size: 20px;
      line-height: 25px;
      font-family: 'PT Sans';
      padding: 29px 0 23px 48px;
      cursor: pointer;

      &:focus {
        outline: none;
      }
    }

    button {
      border: none;
      border-radius: 50px;
      background-color: $blue;
      color: white;
      font-family: 'Montserrat';
      font-weight: 700;
      font-size: 19.86px;
      line-height: 20px;
      width: 259px;
      cursor: pointer;
    }
  }
}

.row {
  display: flex;

  &:first-of-type {
    column-gap: 80px;
  }

  &:last-of-type {
    justify-content: space-between;
    align-items: center;
  }
}
.column {
  display: flex;
  flex-direction: column;
}

.any-questions-title {
  font-family: 'Montserrat Alternates';
  font-size: 48px;
  line-height: 59px;
  margin-bottom: 33px;
}

.leave-a-request {
  font-size: 24px;
  line-height: 36px;
}

.horizontal-line {
  margin: 96px 0 55px;
  border: 1px dashed #ffffff;
}

.agreement {
  margin-top: 38px;
  width: 436px;
  font-size: 14px;
  line-height: 20px;
}

.years {
  margin-top: 15px;
  font-weight: 300;
  font-size: 12px;
}

.logo {
  cursor: pointer;
}

.phone-number {
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  text-align: right;
}

.email {
  text-align: right;
  font-weight: 600;
  font-size: 15px;
  line-height: 18px;
  text-decoration: underline;
}

@media (max-width: $first-media-width) {
  .row {
    padding: 0 51px 0 44px;
  }
}
@media (max-width: 1105px) {
  .row {
    flex-direction: column;
    align-items: center;

    .any-questions-title {
      text-align: center;
    }
    .arrow {
      display: none;
    }
    
    .agreement {
      text-align: center;
    }

    &:first-of-type {
      .column {
        align-items: center;


        .leave-a-request {
          margin-bottom: 64px;
        }
        .input-title {
          display: none;
        }

        .input-container {
          display: flex;
          flex-direction: column;
          row-gap: 23px;

          input {
            margin: 0;
            width: 343px;
          }

          .call-me-btn {
            width: auto;
            min-height: 77px;
            margin-bottom: 30px;
          }
        }

        .agreement {
          margin-top: 150px;
        }
      }
    }
    &:last-of-type {
      row-gap: 27px;
      .socials-column {
        order:  5;
      }
      .column {
        text-align: center;


        a{
          align-self: center;
        }
      }
    }
  }
}
@media (max-width: 434px) {
  .agreement {
    font-size: 11px;
    width: auto;
  }
}
</style>

