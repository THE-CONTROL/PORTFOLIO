<template>
  <div class="w-11/12 m-auto sm:flex">
    <div class="sm:py-10 sm:w-1/2 w-full sm:px-4">
      <div class="bg-gradient-to-r from-gray-400 to-gray-100 rounded-full w-fit sm:w-full p-5 m-auto mt-8 sm:mt-0">
        <img class="sm:w-full sm:h-[400px] rounded-full w-[189px] h-[214px]" 
        src="https://res.cloudinary.com/de49puo0s/image/upload/v1697884155/gloaysc8nlrnimvcxwmi.jpg" 
        alt="Logo"/>     
      </div>
    </div>
    <div class="sm:w-1/2 w-full sm:pt-28 pt-8 text-white">
      <div class="w-fit m-auto text-center sm:text-left">
        <h1 class="font-semibold text-3xl md:text-4xl">{{ introText.start }}
          <br>{{ introText.mid }}
          <br>{{ introText.name }}
        </h1>
      </div>
      <div class="h-40 w-fit mx-auto mt-[30px]">
        <div class="w-fit flex justify-start">
          <button v-for="(item, index) in btnText.box1" :key="index" 
          class="sm:w-[140px] w-[124px] h-[50px] rounded-md md:w-[170px]" :class="index == 0 ?  item.col :
           item.col" @click="scroll(item.val)">{{item.text}}</button>
        </div>
        <div class="mt-3">
          <button class="sm:w-[300px] w-[255px] md:w-[364px] h-[50px] bg-[#414141] hover:bg-[#696969] 
          rounded-md"><fa :icon="['fab', 'github']"/> {{btnText.box2.gitContact}}</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import myMixin from "../mixins/myMixin.js"
export default {
    name: "HomePage",
    mixins: [myMixin],
    setup() {
      const introText = {"start": "Hello, I'm a", "mid": "Web Developer", "name": "Lawson Ekhorutomwen"}
      const btnText = {
        "box1": [
            {
              "text": "Contact me", 
              "col": "bg-[#7996FC] mr-2 px-1 sm:mr-5 md:mr-6 hover:bg-[#416afd]",
              "val": 3770
            }, 
            {
              "text": "Portfolio", 
              "col": "bg-[#414141] hover:bg-[#696969]",
              "val": 1900
            }
        ],
        "box2": {
          "gitContact": "Check out my github",
        }
      }

      return { introText, btnText }
    }
}
</script>

<style>

</style>