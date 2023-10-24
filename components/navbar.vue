<template>
  <div class="w-[451px] h-[29px] m-auto flex justify-between">
    <h1
      v-for="(item, index) in navText"
      :key="index"
      @click="scroll(item.value)"
      class="text-[20px] hover:text-[22px] text-[#C9C9C9] hover:text-[#ececec]"
    >
      {{ item.name }}
    </h1>
  </div>
</template>

<script>
import myMixin from "../mixins/myMixin.js";

export default {
  name: "NavBar",
  mixins: [myMixin],
  setup() {
    const navText = [
      {
        name: "About",
        value: 685,
      },
      {
        name: "Education",
        value: 960,
      },
      {
        name: "Skills",
        value: 1240,
      },
      {
        name: "Portfolio",
        value: 1455,
      },
      {
        name: "Contact",
        value: 3000,
      },
    ];

    return { navText };
  },
};
</script>

<style></style>
