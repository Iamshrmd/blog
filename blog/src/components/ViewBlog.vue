<template>

    <main>
        <div class="grid justify-center p-5">
            <div class="container w-full p-5 border-2 border-solid border-[#444] rounded-xl mt-40">
                <div class="container-content flex flex-col gap-y-6">
                    <div class="content flex flex-col gap-y-3">
                        <img class="w-6 h-6" @click="exitClicked" src="../assets/img/icons8-close-window-26.png" :class="{'hidden' : !darkMode}" alt="exit">
                        <img class="w-6 h-6" @click="exitClicked" src="../assets/img/icons8-exit-50-black.png" :class="{'hidden' : darkMode}" alt="exit">
                            <div class="text flex flex-col gap-y-3 md:gap-x-2">
                                <img class="xs:w-full md:h-64 object-cover position-center md:opacity-50 rounded-xl" src="../assets/img/0.jpg" :class="{'!opacity-100' : !darkMode}">
                                <div>
                                    <h3 class="text-[#fff]" :class="{'!text-[#000]' : !darkMode}">{{ blog.title}}</h3>
                                    <p class="text-[#B8B8BE] text-lg md:text-base" :class="{'!text-[#000]' : !darkMode}">{{ blog.description }}</p>
                                </div>
                            </div>
                    </div>
                    <div  class="subjects">
                        <label class="bg-[#4b6bfb7c] text-[#fff] rounded border-none mr-3 py-1 px-2 " :class="{'!bg-[#314493]' : !darkMode}">{{ blog.subjects }}</label>
                    </div>
                </div>
            </div>
        </div>
    </main>

</template>

<script>
export default {
    props: ['blog','darkMode'],
    methods: {
        exitClicked() {
            this.$emit('exit')
        }
    }

}
</script>

<!-- <style scoped>
:root{
    --dark-color:#;
    --gray-color:#444;
    --light-blue-color:#4b6bfb7c;
    --light-color-op:#ffffff93;
    --p-color:#B8B8BE;
    --light-color:#fff;

}
.container{
        width:100%;
        padding: 20px 20px;
        margin: 50px ;
        border: 1px solid var(--gray-color);
        border-radius: 8px;
        display: flex;
        flex-direction: column;
        row-gap: 15px;
        justify-content: space-between;
    }
    .content{
        display: flex;
        align-items: flex-start;
    }
    img{
        width: 20px;
        height: 20px;
    }
    h3{
        margin: 0;
    }
</style> -->