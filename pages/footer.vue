<template>
  <div class="bg-[#414141] text-white rounded-t-3xl">
    <div class="w-full mt-16 sm:flex text-lg py-8">
        <div class="sm:w-1/2 w-full h-full sm:pl-10 text-center sm:text-left">
            <div>
                <h4 v-for="(item, index) in firstInfo.main" :key="index">{{ item }}</h4>
            </div>
            <a v-for="(item, index) in firstInfo.sec" :key="index" 
            :href="item.address" class="hover:text-blue-400 overflow-clip block"
            :class="index == 0 ? 'my-3' : ''">{{ item.name }}</a>
        </div>
        <div class="sm:w-1/2 w-full sm:flex">
            <div class="sm:w-1/3 w-full h-full mt-10 sm:mt-0 text-center">
                <h3 class="font-medium">Portfolio</h3>
                <div class="w-full">
                    <a v-for="(item, index) in projects" :key="index" :href="item.website">
                        <h5 class="text-[#C9C9C9] text-base my-2 overflow-clip 
                        hover:text-blue-400 px-2">{{ item.name }} Project</h5></a>
                </div>
            </div>
            <div class="sm:w-2/3 w-full h-full mt-10 sm:mt-0 text-center">
                <h3 class="font-medium">Social Media</h3>
                <div class="w-full">
                    <a v-for="(item, index) in contacts" :key="index" :href="item.website">
                        <h5 class="text-[#C9C9C9] text-base my-2 overflow-clip hover:text-blue-400 px-2">
                            <span :class="item.des">
                                <fa :icon="[item.type, item.icon]"/></span> {{ item.name }}</h5></a>
                </div>
            </div>
        </div>
    </div>
    <div class="w-full flex justify-end pr-20 pb-4">
        <div class="font-bold w-fit text-sm p-1 text-center">
            <img src="https://res.cloudinary.com/de49puo0s/image/upload/v1697884155/gloaysc8nlrnimvcxwmi.jpg" 
            class="h-5 w-5 mr-2 float-left rounded-lg " alt="Logo"/>
        </div>
    </div>
    <div class="w-fit hidden fixed sm:block right-10 bottom-5">
        <button class="p-2 text-3xl hover:text-blue-700" @click="scrollUp()"><fa :icon="['fas', 'arrow-up']"/></button>
    </div>
  </div>
</template>

<script>
import myMixin from "../mixins/myMixin.js"

export default {
    name: "FooterPage",
    mixins: [myMixin],
    setup() {
        const firstInfo = {
            "main": [
                "Based in Benin City,",
                "Nigeria",
            ],
            "sec": [
                {   
                    "name": "+234-703-884-1229",
                    "address": "tel:+234-703-884-1229",
                },
                {
                    "name": "clinquant-churros-17d5a7.netlify.app",
                    "address": "https://clinquant-churros-17d5a7.netlify.app/"
                }
            ]
        }
        const projects = ([ 
            {"name": "Pygame", "website": "https://github.com/THE-CONTROL/Pygame-Project"},
            {"name": "Broker Client", "website": "https://gleaming-bavarois-a1b650.netlify.app/"},
            {"name": "Broker Admin", "website": "https://transcendent-cucurucho-a823ad.netlify.app/"},
            {"name": "Forum", "website": "https://profound-buttercream-2a096d.netlify.app/"},
            {"name": "Forum Admin", "website": "https://voluble-cobbler-83c268.netlify.app/"},
            {"name": "Gallery", "website": "https://elegant-arithmetic-273a5c.netlify.app/"},
            {"name": "Church Database", "website": "https://magnificent-truffle-0e4787.netlify.app/"},
            {"name": "Portfolio", "website": "https://clinquant-churros-17d5a7.netlify.app/"}
         ])
        const contacts = ([ 
            {"name": "@LawsonEkho", "website": "https://www.instagram.com/lawsonekho", 
            "type": "fab", "icon": "instagram", "des":"text-white"},
            {"name": "@LawsonEkho", "website": "https://twitter.com/LawsonEkho?t=Vrqd66efsxloF-ca84jkqQ&s=08", 
            "type": "fab", "icon": "twitter", "des": "text-blue-600"},
            {"name": "Lawson Ekhorutomwen", "website": "https://www.linkedin.com/in/lawson-ekhorutomwen-26aa5123b", 
            "type": "fab", "icon": "linkedin", "des": "bg-blue-600 text-white"},
            {"name": "THE-CONTROL", "website": "https://github.com/THE-CONTROL", "type": "fab", 
            "icon": "github", "bg": "text-white"},
            {"name": "lawsonekhorutomwen@gmail.com", "website": "https://elaborate-medovik-171096.netlify.app/", 
            "type": "fas", "icon": "envelope", "des": "text-white"}
         ])

        return { firstInfo, projects, contacts }
    }
}
</script>

<style>

</style>