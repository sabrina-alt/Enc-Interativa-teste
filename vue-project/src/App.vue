<template>
  <div>
    <HeaderIndex />
    <PromotionAndCampaignIndex />
    <FeaturesSection />
    <FeaturesDashboardIndex />
    <SecuritySectionIndex />
    <PlansAndPricesIndex />
    <GlobalFooter />
  </div>
</template>
<script>
import PromotionAndCampaignIndex from "./components/promotionsAndCampaignSection/PromotionAndCampaignIndex.vue";
import HeaderIndex from "@/components/global/HeaderIndex.vue";
import FeaturesSection from "@/components/featuresSection/FeaturesSection.vue";
import FeaturesDashboardIndex from "@/components/featuresDashboardSection/FeaturesDashboardIndex.vue";
import SecuritySectionIndex from "@/components/securitySection/SecuritySectionIndex.vue";
import PlansAndPricesIndex from "@/components/plansAndPricesSection/PlansAndPricesIndex.vue";
import GlobalFooter from "@/components/global/GlobalFooter.vue";

export default {
  components: {
    HeaderIndex,
    PromotionAndCampaignIndex,
    FeaturesSection,
    FeaturesDashboardIndex,
    SecuritySectionIndex,
    PlansAndPricesIndex,
    GlobalFooter,
  },
};
</script>
<style scoped>
body {
  margin: 0;
  padding: 0;
  overflow: hidden;
}
</style>
