<template>
    <div class="container mx-auto">
        <div class="text-center flex flex-col items-center p-10 gap-16">
            <p class="text-lg w-[55%] mt-24">
                Remember the days when you couldn’t find the proper translation of an English word to the Uzbek language? I
                also
                know those feelings when you run against the lack of general use dictionaries - not to mention the
                specialized
                ones, a total absence of online resources in Uzbek, a pre-requisite of knowing the Russian language in order
                to
                apply indirect translation (EN RU UZ and vice versa).
            </p>
            <hr class="border border-1 border-solid border-[#DDDDDD] h-0 w-[100%]">
            <div class="flex w-[100%] justify-between">
                <h1 class="text-[#01756C] text-xl font-semibold">Book edition</h1>
                <p class="text-base w-[60%] text-justify">To reverse the situation, it was decided to compile a large
                    English-Uzbek-English dictionary and the work
                    started back in 2003. 2 years later, the first edition of the bilingual dictionary was published in
                    G’afur G’ulom publishing house; it is still available for sale online. Much attention was directed to
                    the Uzbek-English part; even now, it is the most comprehensive and complete UZ-EN dictionary.
                    A mobile app for Android devices was launched based on the dictionary with ma jor update of the lexical
                    database.
                </p>
            </div>
            <div class="flex w-[100%] justify-between">
                <h1 class="text-[#01756C] text-xl font-semibold">Website dictionary</h1>
                <p class="text-base w-[60%] text-justify">However, we still desperately needed a high-quality online
                    dictionary for English-Uzbek language pair that could cover both everyday and area-specific vocabulary.
                    In September 2022, on the date of 31th anniversary of Independence of Uzbekistan, Leksika.uz was
                    successfully launched.
                    Leksika.uz has mainly been designed to give English learners of any level the help they need to read,
                    speak and write English more effectively. It is also intended to assist translators and localizers by
                    providing useful tips and rules of thumb; these can be found in Localization section.
                </p>
            </div>
            <div class="flex w-[100%] justify-between">
                <h1 class="text-[#01756C] text-xl font-semibold">Prospects</h1>
                <ul class="text-base w-[60%] text-justify list-disc">
                    <li>Russian-Uzbek-Russian dictionary section with largest database on the web;</li>
                    <li>content for easier learning of English, including grammar, writing tips, learning new words;</li>
                    <li>useful tips and motivational articles for freelancers;</li>
                    <li>articles for localizers to Uzbek language, including intricacies of Uzbek grammar;</li>
                    <li>and much more.</li>
                </ul>
            </div>
            <hr class="border border-1 border-solid border-[#DDDDDD] h-0 w-[100%]">
            <div class="flex justify-between w-[100%]">
                <h1 class="text-[#01756C] text-xl font-semibold">Our team</h1>
                <div class="flex w-[60%] h-[64vh] justify-between mb-20">
                    <div @click="toggleModal1"
                        class="bg-white rounded-2xl flex flex-col items-center gap-3 hover:cursor-pointer">
                        <img src="../../assets/photo1.png" alt="">
                        <div class="flex flex-col items-center pb-3 gap-2">
                            <h1 class="text-2xl font-semibold">Akbar Kholmurodov</h1>
                            <hr class="border border-1 border-solid border-[#01756C] w-[50%]">
                            <h2 class="text-[#8C8B8B] text-lg">Founder and content manager</h2>
                        </div>
                    </div>
                    <div @click="toggleModal2"
                        class="bg-white rounded-2xl flex flex-col items-center gap-3 hover:cursor-pointer">
                        <img src="../../assets/photo2.png" alt="">
                        <div class="flex flex-col items-center pb-3 gap-2">
                            <h1 class="text-2xl font-semibold">Asqar Arslonov</h1>
                            <hr class="border border-1 border-solid border-[#01756C] w-[50%]">
                            <h2 class="text-[#8C8B8B] text-lg">Full-Stack (MERN) Developer</h2>
                        </div>
                    </div>
                </div>
                <div
                    :class="modal1 ? 'fixed z-50 flex items-center justify-center bg-[#8080806d] w-full p-4 overflow-x-hidden overflow-y-auto md:inset-0 h-[calc(100%-1rem)] max-h-full' : 'hidden'">
                    <div class="relative w-full max-w-2xl max-h-full">
                        <div class="relative bg-white rounded-lg shadow text-justify">
                            <div class="flex items-start justify-between p-4 border-b rounded-t ">
                                <h3 class="text-xl font-semibold">
                                    Akbar Kholmurodov
                                </h3>
                                <button @click="toggleModal1" type="button"
                                    class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white"
                                    data-modal-hide="defaultModal">
                                    <svg aria-hidden="true" class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path fill-rule="evenodd"
                                            d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                                            clip-rule="evenodd"></path>
                                    </svg>
                                </button>
                            </div>
                            <div class="p-6 space-y-6">
                                <p class="text-base">
                                    Having graduated the International Economic Relations department of the University of
                                    World
                                    Economy
                                    and
                                    Diplomacy in 2001, Akbar dedicated his later years to translation and localization. When
                                    working as
                                    a
                                    translator in various huge projects, he faced the difficulty in finding reliable sources
                                    that can be
                                    used in translation to/from Uzbek language, and as a result some books for English
                                    learners
                                    and
                                    translators were published
                                </p>
                                <h4 class="text-base font-medium">English-Uzbek-English dictionary (book, app)</h4>
                                <h4 class="text-base font-medium">English Grammar for Uzbek Learners (book, app)</h4>
                            </div>
                        </div>
                    </div>
                </div>
                <div
                    :class="modal2 ? 'fixed z-50 flex items-center justify-center bg-[#8080806d] w-full p-4 overflow-x-hidden overflow-y-auto md:inset-0 h-[calc(100%-1rem)] max-h-full' : 'hidden'">
                    <div class="relative w-full max-w-2xl max-h-full">
                        <div class="relative bg-white rounded-lg shadow text-justify">
                            <div class="flex items-start justify-between p-4 border-b rounded-t ">
                                <h3 class="text-xl font-semibold">
                                    Asqar Arslonov
                                </h3>
                                <button @click="toggleModal2" type="button"
                                    class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white"
                                    data-modal-hide="defaultModal">
                                    <svg aria-hidden="true" class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path fill-rule="evenodd"
                                            d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                                            clip-rule="evenodd"></path>
                                    </svg>
                                </button>
                            </div>
                            <div class="p-6 space-y-6">
                                <p class="text-base">
                                    Having started his IT-education at the age of 12, Asqarjon has reached the level of
                                    full-stack developer just 2 years later. Taking several online courses (Technical
                                    Support Fundamentals, Computer Networking) was followed by successful completion of
                                    Front-End Development and Back-End Development courses at the Open Web Academy education
                                    center in Qarshi city. Being an eighth-grader, he is fully responsible for the technical
                                    support of Leksika.uz
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const modal1 = ref(false);
const toggleModal1 = () => {
    modal1.value = !modal1.value;
};
const modal2 = ref(false);
const toggleModal2 = () => {
    modal2.value = !modal2.value;
};
</script>

<style lang="scss" scoped></style>