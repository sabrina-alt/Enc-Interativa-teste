<template>
  <section>
    <div class="text-section">
      <span class="orange-text">FEATURES</span>
      <h2>Lorem ipsum dolor sit amet, consectetur.</h2>
      <span class="description-text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur hendrerit orci
        at Pellentesque porta ullamcorper nisl,
      </span>
    </div>
    <div class="menu-options-section">
      <ul>
        <li
          v-for="(item, index) in itemsDashboard"
          :key="index"
          :class="item.customizedClass ? 'orange-button' : 'regular-button'"
        >
          <img :src="item.iconPath" />
          <div>{{ item.text }}</div>
        </li>
      </ul>
    </div>
    <div class="img-section">
      <img src="@/assets/img/secondDashboardImg.png" />
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      itemsDashboard: [
        {
          iconPath: "public/icons/chart-timeline-variant-shimmer.svg",
          text: "Dashboard",
          customizedClass: true,
        },
        {
          iconPath: "public/icons/application-edit.svg",
          text: "Customização",
        },
        {
          iconPath: "public/icons/cog.svg",
          text: "Configurações",
        },
        {
          iconPath: "public/icons/connection.svg",
          text: "Integração",
        },
        {
          iconPath: "public/icons/tooltip-text.svg",
          text: "Atendimento",
        },
      ],
    };
  },
};
</script>
<style scoped lang="scss">
section {
  display: flex;
  max-width: 100vw;
  min-height: 100%;
  padding-bottom: 5%;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-color: $background-color-dark;
  font-family: $font-primary;
}
.text-section {
  width: 30vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
  text-align: center;
}
.orange-text {
  padding-top: 10vh;
  font-size: $font-size-base;
  font-weight: $font-weight-semi-bold;
  color: $primary-color;
}
h2 {
  font-size: $font-size-medium;
  font-weight: $font-weight-regular;
  color: $whiter-font-color;
  line-height: 56px;
}
.description-text {
  padding: 20px;
  line-height: 22px;
}
.img-section {
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 100%;
  position: relative;
  border: 1px solid $color-border-image;
  border-radius: 8px;
}

.img-section img {
  width: 1061px;
  height: auto;
  overflow: hidden;
  object-fit: cover;
  object-position: top;
}
.menu-options-section {
  padding: 10px 0 20px 0;
  width: 100%;
  display: flex;
  justify-content: center;
}
.menu-options-section ul {
  width: 70vw;
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 8px;
}
.menu-options-section li {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: nowrap;
  overflow: hidden;
  min-width: 187px;
  height: 44px;
  border-radius: 8px;
  gap: 8px;
  font-size: $font-size-base;
  font-weight: $font-weight-plus;
}
.orange-button {
  color: $whiter-font-color;
  background-color: $primary-color;
}
.regular-button {
  color: $ligher-shade-of-gray;
}
</style>
