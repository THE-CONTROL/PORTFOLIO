<template>
  <div class="w-full sm:px-20 text-lg sm:text-">
    <h3 class="font-light leading-tight text-[#C9C9C9] sm:pl-20 pl-12">{{ quoteAuthor }}</h3>
    <blockquote class="text-center sm:text-left font-medium text-white px-5">
        <i><q>{{ theQuote }}</q></i></blockquote>
  </div>
</template>

<script>
export default {
    name: "MyQuote",
    setup() {
        const quoteAuthor = "P.T. Barnum:"
        const theQuote = "If I shoot at the sun, I might hit a star."

        return { quoteAuthor, theQuote }
    }
}
</script>

<style>

</style>