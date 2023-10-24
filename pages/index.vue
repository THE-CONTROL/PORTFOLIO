<template>
  <div>
    <div v-if="load" class="w-screen h-screen bg-black">
      <div class="w-fit mx-auto text-white pt-52">
          <img
            src="https://res.cloudinary.com/de49puo0s/image/upload/v1697884155/gloaysc8nlrnimvcxwmi.jpg"
            class="h-32 w-32 mr-2 float-left rounded-lg object-cover"
            alt="Logo"
          />
      </div>
    </div>
    <div v-else class="bg-[#2D2D2D] pt-[26px]">
      <Nav class="hidden sm:flex" />
      <HomePage />
      <MyQuote />
      <AboutPage />
      <EducationPage />
      <SkillsPage />
      <PortfolioPage />
      <FooterPage />
    </div>
  </div>
</template>

<script>
import Nav from "../components/navbar.vue";
import HomePage from "./home.vue";
import MyQuote from "../components/quote.vue";
import AboutPage from "./about.vue";
import EducationPage from "./education.vue";
import SkillsPage from "./skills.vue";
import PortfolioPage from "./portfolio.vue";
import FooterPage from "./footer.vue";
import { onMounted, ref } from "vue";

export default {
  name: "IndexPage",
  components: {
    Nav,
    HomePage,
    MyQuote,
    AboutPage,
    EducationPage,
    SkillsPage,
    PortfolioPage,
    FooterPage,
  },
  setup() {
    const load = ref(true);

    function setLoad() {
      load.value = false;
    }

    onMounted(() => {
      setTimeout(setLoad, 5000);
    });

    return { load, setLoad };
  },
};
</script>

<style>
::-webkit-scrollbar {
  height: 5px;
  width: 5px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background: #888;
}

::-webkit-scrollbar-thumb:hover {
  background: #555;
}
</style>
