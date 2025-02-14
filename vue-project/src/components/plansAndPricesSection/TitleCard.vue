<template>
  <div class="title-section">
    <h4>{{ title }}</h4>
    <span>{{ price }}</span>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      default: "",
    },
    price: {
      type: String,
      default: "",
    },
  },
};
</script>
<style scopped lang="scss">
.title-section {
  width: 273px;
  height: 67px;
  margin: 25px 30px 10px 25px;
}
h4 {
  color: $primary-color;
  font-weight: $font-weight-regular;
  font-size: $font-size-regular;
  line-height: 38px;
}
.title-section span {
  color: $whiter-font-color;
  font-weight: $font-weight-plus;
  font-size: 24px;
  line-height: 28px;
}
</style>
