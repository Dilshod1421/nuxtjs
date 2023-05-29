<template>
    <header class="bg-[#01756C] w-full fixed">
        <div class="container mx-auto">
            <nav class="flex justify-between items-center h-[80px]">
                <nuxt-link class="logo" to="/"><img src="../assets/logo.svg" alt=""></nuxt-link>
                <ul class="flex gap-9 items-center text-[16px] text-white">
                    <li><nuxt-link class="px-4 py-2 flex gap-2" to="/en-uz">ENG<img src="../assets/vector.svg" alt="">UZB</nuxt-link>
                    </li>
                    <li><nuxt-link class="px-4 py-2" to="/articles">ARTICLES</nuxt-link></li>
                    <li><nuxt-link class="px-4 py-2" to="/grammar">GRAMMAR</nuxt-link></li>
                    <li><nuxt-link class="px-4 py-2" to="/about-us">ABOUT US</nuxt-link></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.router-link-exact-active {
    border: 2px solid #4fa69f;
}

.logo {
    border: none !important;
}
</style>