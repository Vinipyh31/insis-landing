<template>
  <section class="dont-overpay">
    <div class="content">
      <div class="row">
        <img src="@/assets/images/overpay.png" alt="logo" class="title-img" />
        <div class="column">
          <span class="title"
            ><span class="green-text">Не переплачивайте!</span><br />За то, что
            другие навязывают.
          </span>
          <p>
            <b>Рациональной потребление</b> – пользоваться тем, что
            действительно надо
          </p>
        </div>
      </div>
      <div class="row">
        <div class="row__item">
          <div class="circle">
            <img src="@/assets/images/stonks.svg" alt="stonks" />
          </div>
          <span>
            Только<br />
            <span class="green-text">необходимая</span><br />
            скорость
          </span>
        </div>
        <div class="row__item">
          <div class="circle">
            <img src="@/assets/images/pig.svg" alt="stonks" />
          </div>
          <span>
            Только<br />
            <span class="green-text">разумная</span><br />
            цена
          </span>
        </div>
        <div class="row__item">
          <div class="circle">
            <img src="@/assets/images/terms.svg" alt="stonks" />
          </div>
          <span>
            Только<br />
            <span class="green-text">выгодные</span><br />
            условия
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: 'DontOverpaySection',
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';
.dont-overpay {
  padding: 68px 0 154px;
  background-color: $brown;
  color: white;

  .green-text {
    color: #7dcb39;
    font-weight: 700;
  }
  .row {
    display: flex;
    justify-content: space-between;

    &:not(:first-of-type) {
      margin-top: 116px;
    }

    &__item {
      display: flex;
      column-gap: 37px;
      align-items: center;

      .circle {
        position: relative;
        border-radius: 50%;
        width: 86px;
        height: 86px;
        background-color: $beige;

        img {
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
        }
      }

      span {
        font-family: 'Montserrat Alternates';
        font-style: normal;
        font-weight: 600;
        font-size: 22px;
        line-height: 27px;
      }
    }

    .column {
      width: 610px;
      margin-top: 84px;
      .title {
        font-family: 'Montserrat Alternates';
        font-weight: 400;
        font-size: 48px;
        line-height: 59px;
      }
      p {
        margin-top: 41px;
        font-size: 24px;
        line-height: 39px;
      }
    }
  }
}

@media (max-width: 1050px) {
  .dont-overpay .row {
    justify-content: space-around;
    .row__item {
      flex-direction: column;
      row-gap: 25px;
      span {
        font-size: 16px;
        line-height: 20px;
      }
    }
  }

  .dont-overpay {
    .row {
      .title-img {
        height: 300px;
      }
      .column {
        width: 365px;
        margin-top: 0;

        .title {
          font-size: 32px;
          line-height: 39px;
          letter-spacing: -0.02em;
        }

        p {
          font-size: 20px;
          line-height: 30px;
        }
      }
    }
  }
}
@media (max-width: $second-media-width) {
  .dont-overpay {
    .row {
      .title-img {
        height: 114px;
        margin-right: 19.5px;
      }
    }
  }
}
@media (max-width: $first-media-width) {
  .content {
    padding-left: 54px;
    padding-right: 41px;
  }
}
@media (max-width: 512px) {
  .content {
    padding: 0;
  }

  .dont-overpay .row .column {
    width: auto;

    .title {
      font-size: 25px;
    }

    p {
      font-size: 15px;
    }
  }

  .row-item {
    span {
      font-size: 10px;
    }
  }
}
</style>