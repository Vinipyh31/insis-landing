<template>
  <section class="main-section jagged">
    <div class="main-section__content">
      <div class="main-section__content__row">
        <img src="~/assets/images/logo.svg" alt="logo" class="logo" />
        <a href="tel:+88002506060" class="phone-number">8 800 250 60 60</a>
      </div>
      <div class="main-section__content__main-row">
        <div class="main-section__content__column">
          <span class="main-section__content__title"
            >За <span class="green-text">разумное</span> потребление</span
          >
          <div class="row">
            <div class="green-dash"></div>
            <span
              >до <strong>100 Мбит/с</strong> + от <strong>150 каналов</strong>
              <br />Первый месяц бесплатно</span
            >
          </div>
          <button class="btn">Оставить заявку</button>
        </div>
        <img src="~/assets/images/planet.png" alt="planet" class="planet" />
      </div>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: 'MainSection',
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';
.logo {
  cursor: pointer;
  color: #5e4f47;
  fill: #5e4f47;
}

.btn {
  background-color: $blue;
  width: 275px;
  height: 77px;
  color: white;
  font-size: 20px;
  font-weight: 700;
  border-radius: 50px;
  outline: none;
  border: none;
  cursor: pointer;
}

.green-dash {
  width: 38px;
  height: 8px;
  background-color: $green;
  margin-top: 18px;
  margin-right: 28px;
}

.green-text {
  color: $green;
}

.main-section {
  padding: 71px 42px 42px;
  color: $brown;
  margin: 0;

  .btn {
    margin-top: 60px;
    font-family: 'Montserrat';
  }

  .planet {
    z-index: 0;
  }

  &__content {
    width: 1300px;
    margin: 0 auto;

    &__main-row {
      margin-top: -30px;
      display: flex;
      align-items: center;
    }

    &__column {
      align-self: flex-start;
      margin: 131px 0 0;

      .row {
        display: flex;
        margin-top: 38px;
        span {
          font-weight: 400;
          font-size: 24px;
          line-height: 39px;
        }
      }
    }

    &__title {
      font-weight: bolder;
      font-size: 64px;
      line-height: 78px;
      font-family: 'Montserrat Alternates';
    }

    &__row {
      display: flex;
      align-items: center;
      justify-content: space-between;

      .phone-number {
        z-index: 1;
        color: $brown;
        text-decoration: none;
        font-weight: 700;
        font-size: 36px;
        line-height: 44px;
        white-space: nowrap;
      }
    }
  }
}

@media (max-width: $first-media-width) {
  .main-section {
    padding: 71px 0 42px 42px;

    .planet {
      margin-left: -70px;
    }
    &__content {
      width: 100%;
      overflow: hidden;
    }
  }
  .phone-number {
    margin-right: 42px;
  }
}
@media (max-width: $second-media-width) {
  .logo {
    height: 49px;
  }

  .main-section {
    .planet {
    }
    &__content {
      &__main-row {
      }

      &__column {
        margin: 131px 0 0;

        .row {
          span {
            font-size: 24px;
            line-height: 39px;
          }
        }
      }

      &__title {
        font-weight: 700;
        font-size: 40px;
        line-height: 49px;
      }

      &__row {
        display: flex;
        align-items: center;
        justify-content: space-between;

        .phone-number {
          font-size: 24px;
          line-height: 29px;
        }
      }
    }
  }
  .phone-number {
    margin-right: 42px;
  }
}

@media (max-width: 503px) {
  .logo {
    height: 30px;
  }

  .main-section__content__row .phone-number {
    font-size: 18px;
  }
}
</style>