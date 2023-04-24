<template>
  <div class="landing">
    <section class="main-section jagged">
      <div class="main-section__content">
        <div class="main-section__content"></div>
        <img src="~/assets/images/planet.png" alt="planet" srcset="">
      </div>
    </section>
    <section class="advantages">
      
    </section>
    <section class="main-section jagged">
      <h1>hello world!</h1>
    </section>
    <section class="footer">

    </section>
  </div>
</template>

<script>
export default {
  name: 'InsisLanding',
}
</script>

<style lang="scss">
.main-section {
  padding: 71px 0 50px;
}

.jagged {
  position: relative;
  background-color: #EDD2C0;

}

.jagged::after {
  content: '';
  position: absolute;
  display: block;
  height: 10px;
  bottom: -10px;
  background-color: inherit;
  /* -height */
  left: 0;
  right: 0;
  /* TODO Add browser prefixes */
  background: linear-gradient(
      45deg,
      transparent 33.333%,
      #EDD2C0 33.333%,
      #EDD2C0 66.667%,
      transparent 66.667%
    ),
    linear-gradient(
      -45deg,
      transparent 33.333%,
      #EDD2C0 33.333%,
      #EDD2C0 66.667%,
      transparent 66.667%
    );
  background-size: 8px 20px;
  /* toothSize doubleHeight */
  background-position: 0 -10px;
  /* horizontalOffset -height */
}

.jagged:not(:first-of-type)::before {
  content: '';
  position: absolute;
  display: block;
  height: 10px;
  top: -10px;
  background-color: inherit;
  transform: rotateX(180deg);
  /* -height */
  left: 0;
  right: 0;
  /* TODO Add browser prefixes */
  background: linear-gradient(
      45deg,
      transparent 33.333%,
      #EDD2C0 33.333%,
      #EDD2C0 66.667%,
      transparent 66.667%
    ),
    linear-gradient(
      -45deg,
      transparent 33.333%,
      #EDD2C0 33.333%,
      #EDD2C0 66.667%,
      transparent 66.667%
    );
  background-size: 8px 20px;
  /* toothSize doubleHeight */
  background-position: 0 -10px;
  /* horizontalOffset -height */
}

.advantages {
  height: 200px;
  background-color: #5E4F47;
}

.footer {
  background-color: #6EA03F;
  height: 300px;
}
</style>