<template>
  <section>
    <article>
      <span class="small-title">SEGURANÇA</span>
      <h2 class="text-title">Lorem ipsum dolor sit amet, consectetur.</h2>
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
    <div class="img-style">
      <img src="@/assets/icon/Group.svg" />
    </div>
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
  height: 800px;
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
  order: 1;
}

article {
  min-width: 50vw;
  display: flex;
  flex-direction: column;
  text-align: left;
  order: 2;
}

p {
  max-width: 580px;
  font-size: $font-size-base;
  font-weight: $font-weight-regular;
  line-height: 22px;
  color: $lighter-font-color;
  padding-bottom: 20px;
}

@media (max-width: 768px) {
  section {
    flex-direction: column;
    height: auto;
    padding: 20px;
    justify-content: flex-start;
  }

  .img-style {
    min-width: 100%;
    margin-bottom: 20px;
  }
  .img-style img {
    width: 327px;
    height: 205px;
  }

  article {
    min-width: 100%;
    order: 1;
    text-align: left;
  }
  .text-title {
    margin-bottom: 80px;
    margin-top: 0;
  }

  .img-style {
    order: 2;
  }

  section h2 {
    text-align: left;
    margin: 20px 0;
  }

  p {
    max-width: 100%;
    text-align: left;
    padding-left: 0;
  }
}
</style>
