<template>
  <section>
    <article>
      <div class="article-section">
        <span>O QUE É O ENCFY</span>
        <h2>Lorem ipsum dolor sit amet, consectetur.</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur hendrerit
          orci at tellus consequat hendrerit. Pellentesque porta ullamcorper nisl, sit
          amet facilisis magna blandit et. Nunc elementum nisl eu quam scelerisque, in
          rhoncus lectus ultricies.
        </p>
        <p style="height: 80px">
          Sed vel molestie lacus. Vivamus dolor tortor, bibendum nec est interdum,
          eleifend gravida sapien. Suspendisse euismod at tellus sed pulvinar
        </p>
        <div class="btn-features">
          <ButtonFeatures />
        </div>
      </div>
    </article>
    <div class="dashboard-img-style">
      <img src="@/assets/img/firstDashboardImg.png" />
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
<style lang="scss" scoped>
@import "@/assets/scss/utils.scss";

section {
  width: 100%;
  margin: 0 auto;
  padding: 0;
  display: flex;
  font-family: $font-primary;
  padding: 70px 20px 70px 50px;
  overflow: hidden;
}

article {
  padding: 90px 0px 70px 80px;
  display: flex;
  flex-direction: column;
  align-items: left;
  width: 65vw;
  height: 50vh;
}

article span {
  @extend .orange-text;
  width: 580px;
  height: 21px;
}

article h2 {
  font-size: $font-size-medium;
  font-weight: $font-weight-regular;
  line-height: 57px;
  width: 580px;
  height: 153px;
}

p {
  color: $lighter-font-color;
  font-size: $font-size-base;
  font-weight: $font-weight-regular;
  width: 580px;
  height: 125px;
  padding: 0;
  margin: 0 auto;
}

.dashboard-img-style {
  left: 10vw;
  position: relative;
}

.dashboard-img-style img {
  object-fit: cover;
  object-position: left;
  overflow: hidden;
  width: 1200px;
  height: 750px;
}
@media (max-width: 768px) {
  section {
    flex-direction: column;
    align-items: center;
    padding: 40px 20px;
  }

  article {
    width: 100%;
    padding: 0 20px;
    text-align: left;
    height: auto;
  }

  article h2,
  article p,
  article span {
    width: 100%;
    height: auto;
  }

  .dashboard-img-style {
    left: 0;
    position: static;
    width: 100%;
    display: flex;
    justify-content: center;
  }

  .dashboard-img-style img {
    width: 341px;
    height: 238.48px;
  }
  .btn-features {
    padding-top: 25px;
  }
}
</style>
