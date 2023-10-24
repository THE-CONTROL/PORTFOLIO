<template>
  <div class="w-full mt-16 sm:px-16 px-4 text-white">
    <h2 class="font-bold text-4xl">Skills</h2>
    <div class="w-full mt-3 flex flex-wrap justify-start">
        <p v-for="(item, index) in skills" :key="index" 
        class="text-center text-lg mx-3">
        {{ item }}</p>
    </div>
  </div>
</template>

<script>
export default {
    name: "SkillsPage",
    setup() {
        const skills = [
            "HTML,", 
            "CSS,", 
            "TailwindCSS,", 
            "Bootstrap,", 
            "Javascript,", 
            "Vue,", 
            "Nuxt,",
            "React,",
            "Next,", 
            "Python,", 
            "Pygame,", 
            "Flask,", 
            "Fast API,", 
            "Solidity",
            "SQL",
            "SQLAlchemy,"    
        ]

        return { skills }
    }
}
</script>

<style>

</style>