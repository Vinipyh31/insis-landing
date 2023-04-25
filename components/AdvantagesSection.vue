<template>
  <section class="advantages jagged">
    <div class="content">
      <div class="title">
        <h1>Интернет + Цифровое <span class="green-text">ТВ</span></h1>
        <span class="title--small">Чистая выгода</span>
      </div>
      <div class=".container">
        <div class="circle big">
          <div class="caption one">
            <div class="caption__content">
              <img src="@/assets/images/satellite.svg" alt="" /><span
                class="caption__content__text"
                ><strong>Хороший</strong> <br />выбор каналов</span
              >
            </div>
            <img src="@/assets/images/line.svg" alt="line" class="line one" />
          </div>
          <div class="caption two">
            <div class="caption__content">
              <img src="@/assets/images/drawn-pc.svg" alt="" /><span
                class="caption__content__text"
                ><strong>Приложение</strong> <br />Инсис ТВ</span
              >
            </div>
            <img src="@/assets/images/line.svg" alt="line" class="line two" />
          </div>
          <div class="caption three">
            <div class="caption__content">
              <img src="@/assets/images/lightning-strike.svg" alt="" /><span
                class="caption__content__text"
                ><strong>Быстрое</strong> <br />подключение</span
              >
            </div>
            <img src="@/assets/images/line.svg" alt="line" class="line three" />
          </div>
          <div class="caption four">
            <div class="caption__content">
              <img src="@/assets/images/smartphone.svg" alt="" /><span
                class="caption__content__text"
                >Надежная<br />тех.поддержка<br />в
                <strong>любое время</strong></span
              >
            </div>
            <img src="@/assets/images/line.svg" alt="line" class="line four" />
          </div>
          <div class="circle medium">
            <div class="circle small">
              <img src="@/assets/images/pc.png" alt="pc" class="pc" />
              <img
                src="@/assets/images/laptop.png"
                alt="laptop"
                class="laptop"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: 'AdvantagesSection',
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';
.advantages {
  background-color: $beige;
  padding: 138px 0;
  color: $brown;
}

.green-text {
  color: $green;
}

.title {
  width: 100%;
  text-align: center;
  h1 {
    font-family: 'Montserrat Alternates';
    font-style: normal;
    font-weight: 400;
    font-size: 48px;
    line-height: 59px;
  }
  &--small {
    display: block;
    font-weight: 400;
    margin: 15px 0;
    font-size: 24px;
    line-height: 29px;
  }
}

.circle {
  background: $beige;
  box-shadow: 0px 14px 223px rgba(0, 0, 0, 0.09);
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;

  &.big {
    position: relative;
    width: 612px;
    height: 612px;
    margin: 70px auto 0;

    .caption {
      z-index: 10;
      position: absolute;

      &.one {
        right: -235px;
        top: -9px;
      }
      &.two {
        top: 33px;
        left: -239px;
      }
      &.three {
        bottom: 48px;
        left: -200px;
      }
      &.four {
        bottom: 56px;
        right: -238px;
      }

      &__content {
        position: relative;
        display: flex;
        align-items: center;
        column-gap: 18px;

        &__text {
          font-size: 24px;
          line-height: 29px;
        }
      }

      .line {
        position: absolute;

        &.one {
          top: 48px;
          left: -132px;
        }
        &.two {
          transform: rotate(232deg);
          top: 54px;
          left: 138px;
        }
        &.three {
          transform: rotate(178deg);
          top: -103px;
          left: 214px;
        }
        &.four {
          transform: rotate(37deg);
          top: -129px;
          left: -55px;
        }
      }
    }
  }
  &.medium {
    width: 496px;
    height: 496px;
  }
  &.small {
    width: 399px;
    height: 399px;
    position: relative;

    .pc {
      position: absolute;
      left: -50px;
      top: -30px;
    }

    .laptop {
      position: absolute;
      right: -110px;
      bottom: -30px;
    }
  }
}

@media (max-width: 1110px) {
  .circle {
    &.big {
      margin-top: 100px;
      width: 372px;
      height: 372px;
      .caption {
        &.one {
          right: -25px;
          top: -78px;
        }
        &.two {
          top: -62px;
          left: -52px;
        }
        &.three {
          bottom: -62px;
          left: -45px;
        }
        &.four {
          bottom: -56px;
          right: -33px;
        }

        &__content {
          &__text {
            font-size: 16px;
            line-height: 20px;
          }
        }

        .line {
          width: 76.58px;

          &.one {
            top: 51px;
            left: -56px;
            transform: rotate(315deg);
          }
          &.two {
            transform: rotate(232deg);
            top: 58px;
            left: 48px;
          }
          &.three {
            transform: scale(-1, 1) rotate(70deg);
            top: -59px;
            left: 91px;
          }
          &.four {
            transform: rotate(72deg);
            top: -75px;
            left: -35px;
          }
        }
      }
    }

    &.medium {
      width: 302px;
      height: 302px;
    }

    &.small {
      width: 242.2px;
      height: 242.2px;

      .pc {
        position: absolute;
        width: 227px;
        left: -35px;
        top: -5px;
      }

      .laptop {
        width: 243px;
        right: -65px;
        bottom: -21px px;
      }
    }
  }
}

@media (max-width: 470px) {
  .circle.big .caption__content__text {
    font-size: 12px;
  }
}
</style>