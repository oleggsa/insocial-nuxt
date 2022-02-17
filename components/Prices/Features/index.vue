<template>
  <div class="features__list">
    <div class="features__item" v-for="item in features" :key="item.name">
      <img :src="item.icon" alt="feature">{{item.name}}
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  props: {
    features: {
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
@import "style";
.features__item {
  display: flex;

}
</style>
