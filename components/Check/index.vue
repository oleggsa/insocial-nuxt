<template>
  <div class="check__wrapper" id="check">
    <div class="check__content-wrapper">
      <div class="check__content-header">
        <p class="check__content-header-header">Check Your Growth</p>
        <div class="check__content-header-group">
          <GradientRectangle></GradientRectangle>
          <p class="check__content-header-desqr">See your account after 30 days with Insocial</p>
        </div>
      </div>
      <div class="check__content-search">
        <input type="text" class="check__content-search-input" placeholder="Enter Instagram account...">
        <div class="check__content-search-btn">
          <a href="#"><span class="check__content-search-btn-text">PREVIEW GROWTH</span></a>
        </div>
      </div>
      <div class="check__content-bottom">
        <p>Up to <span>15x</span> more effective than Instagram Bots</p>
      </div>
    </div>
    <div class="check__images">
      <div class="check__images-phone">
        <lottie
          :options="defaultOptions.phone"
          :height="777"
          :width="777"
        />
      </div>
      <img class="check__images-bottom" src="./../../images/case-bottom.png" alt="bottom">
    </div>
  </div>
</template>

<script>
import GradientRectangle from "~/components/UI/GradientRectangle";
import lottie from 'vue-lottie/src/lottie.vue';
import * as robotAnim from "~/assets/animations/phone.json";

export default {
  name: "Check",
  components: {
    GradientRectangle,
    lottie
  },
  data() {
    return {
      defaultOptions: {
        phone: {
          animationData: robotAnim.default
        }
      },
      animationSpeed: 1
    };
  },
}
</script>

<style lang="scss" scoped>
@import "style";
</style>
