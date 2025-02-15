<template>
  <div class="out-container">
    <div class="main-container">
      <ul>
        <li v-for="(item, index) in plansDetails" :key="index">
          <img src="@/assets/icon/checkIcon.svg" />
          <span>{{ item.description }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    backgroundColor: {
      type: String,
      default: "color-button-grey",
    },
  },
  data() {
    return {
      plansDetails: [
        {
          description: "Uma modalidade de premiação",
        },
        {
          description: "Duas modalidades de premiação",
        },
        {
          description: "Dashboard",
        },
        {
          description: "Ferramenta de atendimento",
        },
        {
          description: "Integrações",
        },
        {
          description: "Até R$ 50.000,00 em premiação",
        },
        {
          description: "Até R$ 90.000,00 em premiação",
        },
        {
          description: "Valor de premiação superior",
        },
      ],
    };
  },
};
</script>
<style scoped lang="scss">
.main-container {
  display: flex;
  flex-direction: column;
  color: $whiter-font-color;
  font-family: $font-primary;
  font-weight: $font-weight-regular;
}
ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 16px;
  padding: 0 0 0px 25px;
  width: 321px;
}
span {
  padding-left: 10px;
}
ul li {
  line-height: 19px;
  font-size: $font-size-base;
}
</style>
