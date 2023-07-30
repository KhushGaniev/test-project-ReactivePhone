<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <h3 :class="$style.title">
          {{ countQuestions }} questions out of
          {{ dataQuestions.length }} passed
        </h3>
        <div :class="$style.progress">
          <div
            v-for="bar in numberOfBars"
            :key="bar"
            :class="[progressBarClass(bar)]"
          ></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import data from "@/data/goods";

export default {
  name: "vProgressBar",
  data() {
    return {
      numberOfBars: 7,
      dataQuestions: JSON.parse(localStorage.getItem("goodsData")) || data,
    };
  },
  computed: {
    countQuestions() {
      return this.dataQuestions.reduce((acc, el) => {
        return acc + el.count;
      }, 0);
    },
    percentageCompleted() {
      return (this.countQuestions / this.dataQuestions.length) * 100;
    },
  },
  methods: {
    progressBarClass(barNumber) {
      if (barNumber <= this.percentageCompleted / (100 / this.numberOfBars)) {
        return this.$style.progressStrip;
      } else {
        return this.$style.progressStripNull;
      }
    },
  },
  mounted() {
    this.countQuestions;
    this.progressBarClass();
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
.progressStripNull {
  height: 100%;
  opacity: 0.1;
  background: var(--color-green, #52a754);
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
