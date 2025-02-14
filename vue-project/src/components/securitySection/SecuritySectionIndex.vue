<template>
  <section>
    <div class="img-style">
      <img src="@/assets/icon/Group.svg" />
    </div>
    <article>
      <span class="small-title">SEGURANÇA</span>
      <h2>Lorem ipsum dolor sit amet, consectetur.</h2>
      <div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur hendrerit
          orci at tellus consequat hendrerit. Pellentesque porta ullamcorper nisl, sit
          amet facilisis magna blandit et. Nunc elementum nisl eu quam scelerisque, in
          rhoncus lectus ultricies.
        </p>
        <p>
          Sed vel molestie lacus. Vivamus dolor tortor, bibendum nec est interdum,
          eleifend gravida sapien. Suspendisse euismod at tellus sed pulvinar. 
        </p>
      </div>
      <div>
        <ButtonFeatures />
      </div>
    </article>
  </section>
</template>
<script>
import ButtonFeatures from "@/components/global/ButtonFeatures.vue";
export default {
  components: {
    ButtonFeatures,
  },
};
</script>
<style scoped lang="scss">
@import "@/assets/scss/utils.scss";
section {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 559px;
}
.small-title {
  @extend .orange-text;
}
section h2 {
  font-size: $font-size-medium;
  font-weight: $font-weight-regular;
  max-width: 580px;
  max-height: 116px;
  line-height: 57px;
  margin: 20px 0 20px 0;
}
.img-style {
  min-width: 45vw;
  display: flex;
  justify-content: center;
  align-items: center;
}
article {
  min-width: 50vw;
  display: flex;
  flex-direction: column;
  text-align: left;
}
p {
  max-width: 580px;
  font-size: $font-size-base;
  font-weight: $font-weight-regular;
  line-height: 22px;
  color: $lighter-font-color;
  padding-bottom: 20px;
}
</style>
