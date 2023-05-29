<template>
    <div class="container mx-auto">
        <div class="flex flex-col items-center justify-evenly">
            <form @submit.prevent="searchWord"
                class="bg-white w-[60%] h-[8vh] rounded-full mt-40 flex justify-between items-center px-1">
                <button
                    class="bg-[#01756C] text-white text-[16px] py-4 w-[150px] rounded-full flex justify-evenly items-center">ENG<img
                        src="../../assets/vector.svg" alt="">UZB</button>
                <img src="../../assets/search.svg" alt="">
                <input v-model="search" class="py-4 w-[78%] rounded-full focus:outline-none" type="text"
                    placeholder="Search words here...">
                <input type="submit" class="hidden">
            </form>
            <div v-if="data.data" class="bg-white w-[60%] rounded-3xl h-[20vh] mt-20 p-6 flex flex-col justify-between">
                <h1 class="text-3xl font-bold">{{ data?.data[0]?.word }}</h1>
                <h3 class="text-[#8C8B8B] text-base italic">{{ data?.data[0]?.meanings[0]?.partOfSpeech }}, {{
                    data?.data[0]?.meanings[2]?.partOfSpeech }}</h3>
                <div class="flex gap-3">
                    <img @click="audioPlay" class="hover:cursor-pointer" src="../../assets/volume.svg" alt="">
                    <h2>{{ data?.data[0]?.phonetics[0]?.text || data?.data[0]?.phonetics[1]?.text }}</h2>
                </div>
            </div>
            <div v-else-if="not_found" class="flex gap-10 w-[64%] items-center mt-16">
                <img src="../../assets/sheksper1.png" alt="">
                <div class="text-center w-[50%]">
                    <h1 class="text-2xl font-bold mb-7">Oops, no such word found!</h1>
                    <h3 class="text-lg">If you believe there is such a word in the language of Shakespeare, please take a
                        few seconds to
                        report it via Telegram or Gmail and we will add it asap!</h3>
                </div>
            </div>
            <div v-else class="text-[24px] text-center w-[35%] mt-36">
                <p>Search any words, and we found this word defination, translation and etc.</p>
            </div>
        </div>
    </div>
</template>

<script setup>
const data = ref('');
const search = ref('');
const not_found = ref(false);
const searchWord = async () => {
    data.value = await useFetch(`https://api.dictionaryapi.dev/api/v2/entries/en/${search.value.toLowerCase()}`)
    if (!data.value.data) {
        not_found.value = !not_found.value;
    }
    search.value = "";
};
const audioPlay = () => {
    if (data.value.data[0]?.phonetics[0]?.audio) {
        const audio = new Audio(data.value.data[0]?.phonetics[0]?.audio);
        audio.play();
    }
}
</script>

<style lang="scss" scoped></style>