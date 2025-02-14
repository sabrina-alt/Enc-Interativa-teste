<template>
  <div>
    <a :class="buttonClasses">{{ text }}</a>
  </div>
</template>
<script>
export default {
  props: {
    color: {
      type: Boolean,
      required: true,
    },
    background: {
      type: Boolean,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      default: "",
    },
    size: {
      type: String,
      default: "",
    },
  },
  computed: {
    buttonClasses() {
      return [
        this.color ? `${this.color}` : "",
        this.background ? `${this.background}` : "",
        this.size ? `${this.size}` : "size-button",
      ];
    },
  },
};
</script>
<style lang="scss">
@import "@/assets/scss/utils.scss";
.medium-size {
  @extend .default-button;
  width: 273px;
  height: 45px;
  font-weight: $font-weight-semi-bold;
  display: flex;
  justify-content: center;
}
.size-button {
  @extend .default-button;
  width: 152px;
  height: 45px;
}
.whiter-font-color {
  color: $whiter-font-color;
}
.darker-font-color {
  color: $darker-font-color;
}
.text-secondary {
  color: #2ecc71;
}
.primary-color {
  background-color: $primary-color;
}
.color-border-button {
  border: 1px solid $color-border-button;
}
.color-button-grey {
  background: $color-button-grey;
}
</style>
