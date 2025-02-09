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

        <p>
          Sed vel molestie lacus. Vivamus dolor tortor, bibendum nec est interdum,
          eleifend gravida sapien. Suspendisse euismod at tellus sed pulvinar
        </p>
        <div>btn Features</div>
      </div>
    </article>
    <div class="dashboard-img-style">
      <img src="@/assets/img/firstDashboardImg.png" />
    </div>
  </section>
</template>
<style lang="scss" scoped>
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
  padding: 90px 20px 70px 80px;
  display: flex;
  flex-direction: column;
  align-items: left;
  width: 628px;
  height: 559px;
}
article span {
  color: $primary-color;
  font-size: $font-size-base;
  font-weight: $font-weight-semi-bold;
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
  height: 154px;
  padding: 0;
  margin: 0 auto;
}
.dashboard-img-style {
  left: 220px;
  position: relative;
}
.dashboard-img-style img {
  object-fit: cover;
  object-position: left;
  overflow: hidden;
  width: 1200px;
  height: 750px;
}
</style>
