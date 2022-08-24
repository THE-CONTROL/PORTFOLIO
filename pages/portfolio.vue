<template>
  <div class="w-full mt-16 sm:px-16 px-4 text-white">
    <h2 class="font-bold text-4xl">Portfolio</h2>
    <div class="w-full flex flex-wrap justify-evenly">
        <a v-for="(item, index) in projects" :key="index" :href="item.website" 
        class="mt-5 hover:bg-[#474747] rounded-lg mx-2">
            <img :src="item.image" :alt="item.name + '' + 'Project Image'" 
            class="w-[254px] h-[153px] rounded-lg hover:opacity-70">
            <h4 class="text-2xl font-semibold text-center">{{ item.name  }} Project</h4>
        </a>
    </div>
  </div>
</template>

<script>
export default {
    name: "PortfolioPage",
    setup() {
        const projects = ([ 
            {"name": "Pygame", "website": "https://github.com/THE-CONTROL/Pygame-Project", 
            "image": require("../assets/portImages/img3.jpg")},
            {"name": "Flask", "website": "https://control.pythonanywhere.com/", 
            "image": require("../assets/portImages/img2.jpg")},
            {"name": "Blog", "website": "https://phenomenal-tartufo-128db5.netlify.app/", 
            "image": require("../assets/portImages/img4.png")},
            {"name": "Gallery", "website": "https://elaborate-medovik-171096.netlify.app/", 
            "image": require("../assets/portImages/fa.jpg")},
         ])

        return { projects }
    }
}
</script>

<style>

</style>