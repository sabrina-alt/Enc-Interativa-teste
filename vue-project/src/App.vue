<template>
  <div>
    <HeaderIndex />
    <PromotionAndCampaignIndex />
    <FeaturesSection />
  </div>
</template>
<script>
import PromotionAndCampaignIndex from "./components/promotionsAndCampaignSection/PromotionAndCampaignIndex.vue";
import HeaderIndex from "@/components/global/HeaderIndex.vue";
import FeaturesSection from "@/components/featuresSection/FeaturesSection.vue";
export default {
  components: {
    HeaderIndex,
    PromotionAndCampaignIndex,
    FeaturesSection,
  },
};
</script>
<style scoped>
body {
  margin: 0;
  padding: 0;
}
</style>
