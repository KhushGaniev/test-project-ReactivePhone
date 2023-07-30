<template>
  <div :class="$style.root">
    <div :class="$style.wrapper">
      <vCard
        v-for="item in arrCard"
        :key="item.id"
        :class="$style.chidrenCard"
        :text="item.text"
        :image="item.image"
      />
    </div>
  </div>
</template>

<script>
import vCard from "@/components/mainLayout/vCard.vue";

export default {
  name: "vCardItems",
  components: {
    vCard,
  },
  data() {
    return {
      arrCard: [
        { id: 1, text: "DVSA Exam", image: "images/iconsCard/dvsa.svg" },
        { id: 2, text: "Express mode", image: "images/iconsCard/rocket.svg" },
        {
          id: 3,
          text: "Hazard perception",
          image: "images/iconsCard/tv.svg",
        },
        { id: 4, text: "Road signs", image: "images/iconsCard/sign.svg" },
        {
          id: 5,
          text: "Multiplayer Learning",
          image: "images/iconsCard/game.svg",
        },
      ],
    };
  },
};
</script>

<style module>
.root {
  margin-top: 8px;
}
.wrapper {
  display: flex;
  flex-wrap: wrap;
  flex-grow: 1;
  gap: 8px;
}
.chidrenCard {
  flex-grow: 1;
  width: 40%;
}
</style>
