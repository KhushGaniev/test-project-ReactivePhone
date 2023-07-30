<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <h3 :class="$style.title">
          {{ this.countQuestions }} questions out of
          {{ this.dataQuestions.length }} passed
        </h3>
        <div :class="$style.progress">
          <div
            v-for="index in numberOfBars"
            :key="index"
            :class="$style.progressStrip"
          ></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import data from "@/data/goods";

export default {
  name: "vProgresBar",
  data() {
    return {
      numberOfBars: 7,
      dataQuestions: JSON.parse(localStorage.getItem("goodsData")) || data,
    };
  },
  computed: {
    countQuestions() {
      const questions = this.dataQuestions.reduce((acc, el) => {
        return acc + el.count;
      }, 0);
      return questions;
    },
  },
  mounted() {
    this.countQuestions;
  },
};
</script>

<style module>
.root {
  margin-top: 8px;
}
.container {
  max-width: 360px;
  margin: 0 auto;
}
.title {
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
}
.progress {
  width: 250px; /* Ширина прогресс-бара */
}

/* Стили для зеленых полосок */
.progressStrip {
  height: 100%;
  background-color: #4caf50; /* Зеленый цвет */
  display: inline-block; /* Отображаем полоски в ряд */
  width: 30px; /* Ширина каждой полоски */
  height: 6px; /* Высота каждой полоски */
  border-radius: 5px; /* Закругление углов */
  margin-right: 5px; /* Интервал между полосками */
}
.progressStrip:last-child {
  margin-right: 0;
}
</style>
