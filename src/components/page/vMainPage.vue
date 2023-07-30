<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <vHeader />
      <vCardLearnProgress />
      <vCardItems />
      <vShapeCard />
      <vFooter />
    </div>
  </div>
</template>

<script>
import vHeader from "@/components/vHeader.vue";
import vCardLearnProgress from "@/components/mainLayout/vCardLearnProgress.vue";
import vCardItems from "@/components/mainLayout/vCardItems.vue";
import vShapeCard from "@/components/mainLayout/vShapeCard.vue";
import vFooter from "@/components/vFooter.vue";

export default {
  name: "vMain",
  components: {
    vHeader,
    vCardLearnProgress,
    vCardItems,
    vShapeCard,
    vFooter,
  },
};
</script>

<style module>
.root {
  background: rgba(249, 249, 249, 1);
  min-height: 100vh;
}
.container {
  max-width: 360px;
  margin: 0 auto;
  padding: 0 16px;
}
</style>
