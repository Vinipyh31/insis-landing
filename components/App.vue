<template>
  <div class="landing">
    <MainSection />
    <DontOverpaySection />
    <AdvantagesSection />
    <FooterSection/>
  </div>
</template>

<script>
import AdvantagesSection from './AdvantagesSection.vue'
import DontOverpaySection from './DontOverpaySection.vue'
import FooterSection from './FooterSection.vue'
import MainSection from './MainSection.vue'

export default {
  name: 'InsisLanding',
  components: { MainSection, DontOverpaySection, AdvantagesSection, FooterSection},
}
</script>

,
    FooterSection<style lang="scss">
@import '@/assets/styles/variables.scss';


.jagged {
  position: relative;
  background-color: $beige;

  &::after {
    content: '';
    position: absolute;
    display: block;
    height: 10px;
    bottom: -10px;
    background-color: inherit;
    left: 0;
    right: 0;
    background: linear-gradient(
        45deg,
        transparent 33.333%,
        #edd2c0 33.333%,
        #edd2c0 66.667%,
        transparent 66.667%
      ),
      linear-gradient(
        -45deg,
        transparent 33.333%,
        #edd2c0 33.333%,
        #edd2c0 66.667%,
        transparent 66.667%
      );
    background-size: 8px 20px;
    background-position: 0 -10px;
  }

  &:not(:first-of-type)::before {
    content: '';
    position: absolute;
    display: block;
    height: 10px;
    top: -10px;
    background-color: inherit;
    transform: rotateX(180deg);
    left: 0;
    right: 0;
    background: linear-gradient(
        45deg,
        transparent 33.333%,
        #edd2c0 33.333%,
        #edd2c0 66.667%,
        transparent 66.667%
      ),
      linear-gradient(
        -45deg,
        transparent 33.333%,
        #edd2c0 33.333%,
        #edd2c0 66.667%,
        transparent 66.667%
      );
    background-size: 8px 20px;
    background-position: 0 -10px;
  }
}
.content {
  width: 1300px;
  margin: 0 auto;
}

@media (max-width: $first-media-width) {
  .content {
    width: 100%;
  }
}
</style>