<template>
  <section class="get-started__wrapper">
    <div class="get-started__content-wrapper">
      <div class="get-started__content">
        <div class="get-started__content-title">
          MARKETING TOOLKIT <br>FOR INSTAGRAM
        </div>
        <div class="get-started__content-desqr">
          Become Instagram-famous and skyrocket sales by using pro tools. These must-have solutions
          will help you attract fans, engage with сustomers, сurate content, and grow revenue.
        </div>
        <div class="get-started__content-btns">
          <CustomButton>GET STARTED</CustomButton>
          <div class="get-started__second-button">
            <CustomButton type="secondary">CHECK YOUR GROWTH</CustomButton>
            <GradientRectangle></GradientRectangle>
          </div>
        </div>
      </div>

      <div class="get-started__images">
        <div class="get-started__images-robot">
          <lottie
            :options="defaultOptions.robot"
            :height="600"
            :width="600"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import GradientRectangle from "~/components/UI/GradientRectangle";
import CustomButton from "~/components/UI/CustomButton";
import lottie from 'vue-lottie/src/lottie.vue';
import * as robotAnim from "~/assets/animations/robot.json";


export default {
  name: "GetStarted",
  components: {
    CustomButton,
    GradientRectangle,
    lottie
  },
  data() {
    return {
      defaultOptions: {
        robot: {
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
