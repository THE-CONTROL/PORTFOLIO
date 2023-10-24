<template>
  <div class="w-full mt-16 sm:px-16 px-4 text-white">
    <h2 class="font-bold text-4xl">Portfolio</h2>
    <div class="w-full flex flex-wrap justify-evenly">
      <a
        v-for="(item, index) in projects"
        :key="index"
        :href="item.website"
        class="mt-5 hover:bg-[#474747] rounded-lg mx-2"
      >
        <img
          :src="item.image"
          :alt="item.name + '' + 'Project Image'"
          class="w-[254px] h-[153px] rounded-lg hover:opacity-70"
        />
        <h4 class="text-2xl font-semibold text-center">
          {{ item.name }} Project
        </h4>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "PortfolioPage",
  setup() {
    const projects = [
      {
        name: "Pygame",
        website: "https://github.com/THE-CONTROL/Pygame-Project",
        image: require("../assets/portImages/img3.jpg"),
      },
      {
        name: "Broker Client",
        website: "https://gleaming-bavarois-a1b650.netlify.app/",
        image: require("../assets/portImages/Broker.jpg"),
      },
      {
        name: "Broker Admin",
        website: "https://transcendent-cucurucho-a823ad.netlify.app/",
        image: require("../assets/portImages/Ad2.jpeg"),
      },
      {
        name: "Forum",
        website: "https://profound-buttercream-2a096d.netlify.app/",
        image: require("../assets/portImages/img4.jpg"),
      },
      {
        name: "Forum Admin",
        website: "https://voluble-cobbler-83c268.netlify.app/",
        image: require("../assets/portImages/Ad1.jpeg"),
      },
      {
        name: "Gallery",
        website: "https://elegant-arithmetic-273a5c.netlify.app/",
        image: require("../assets/portImages/img6.jpg"),
      },
      {
        name: "Church Database",
        website: "https://magnificent-truffle-0e4787.netlify.app/",
        image: require("../assets/portImages/img5.jpg"),
      },
      {
        name: "Portfolio",
        website: "https://clinquant-churros-17d5a7.netlify.app/",
        image: "https://res.cloudinary.com/de49puo0s/image/upload/v1697884155/gloaysc8nlrnimvcxwmi.jpg",
      },
    ];

    return { projects };
  },
};
</script>

<style></style>
