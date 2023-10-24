<template>
  <div class="w-full mt-16 sm:px-16 px-4 text-white">
    <h2 class="font-bold text-4xl">About Me</h2>
    <div class="w-full mt-3">
        <p v-for="(item, index) in text" :key="index" 
        class="text-center text-lg mt-2">
        {{ item }}</p>
    </div>
  </div>
</template>

<script>
export default {
    name: "AboutPage",
    setup() {
        const text = [
            "I am Lawson Ekhorutomwen. I am a full stack web developer and a medical student at the University of Benin (UNIBEN). Although I am currently based in Benin City, Edo State, I am open to remote employment opportunities for companies around the globe.",
            "I have a few personal projects which highlight my skills as a web developer. These can be accessed in my portfolio page.",
            "When I am not glued to my computer screen or reading my medical textbooks, I spend my time watching football, listening to music and watching movies."
        ]

        return { text }
    }
}
</script>

<style>

</style>