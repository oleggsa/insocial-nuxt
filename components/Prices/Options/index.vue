<template>
  <div class="prices__content-options-wrapper">
    <div v-for="item in pricesOptions" :key="item.name" class="prices__content-options">
      <div v-if="item.active === true">
        <CustomSwitch></CustomSwitch>
        <div class="prices__content-text">
          <div class="prices__content-text-header">{{item.name}}</div>
          <GradientRectangle></GradientRectangle>
          <div class="prices__content-text-desqr">{{item.desqr}}</div>
        </div>
        <Counter></Counter>
      </div>
      <div v-else class="prices__content-options">
        <CustomSwitch state="disabled"></CustomSwitch>
        <div class="prices__content-text">
          <div class="prices__content-text-header">{{item.name}}</div>
          <GradientRectangle></GradientRectangle>
          <div class="prices__content-text-desqr">{{item.desqr}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CustomSwitch from "~/components/UI/CustomSwitch";
import Counter from "~/components/UI/Counter";
import GradientRectangle from "~/components/UI/GradientRectangle";

export default {
  name: "index",
  components: {GradientRectangle, Counter, CustomSwitch},
  props: {
    pricesOptions: {
      type: Array,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
@import "style";
</style>
