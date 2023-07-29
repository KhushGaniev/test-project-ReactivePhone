<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <vCardNumber
          v-for="item in goodsData"
          :key="item.id"
          :task="item.task"
          :count="item.count"
          @update:count="updateCount(item, $event)"
        />
      </div>
    </div>
  </div>
</template>

<script>
import vCardNumber from "@/components/taskLayout/vCardNumber";
import data from "@/data/goods";

export default {
  name: "vCardNumberItems",
  components: {
    vCardNumber,
  },
  data() {
    return {
      goodsData: data,
    };
  },
  methods: {
    updateCount(item, newCount) {
      // Обновляем значение count в массиве goodsData
      item.count = newCount;
    },
  },
};
</script>

<style module>
.root {
  padding-top: 45px;
}
.container {
  max-width: 375px;
  margin: 0 auto;
}
.wrapper {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 15px;
}
@media (max-width: 375px) {
  .wrapper {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
}
</style>
