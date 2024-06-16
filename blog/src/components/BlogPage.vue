<script>
import { onMounted } from 'vue';

    export default {
        data() {
            return {
                blogs : [
                    {
                        title:"Flavio Copes' Blog",
                        des:"JavaScript and Web Development Tutorials. Flavio is one of the most recognizable JavaScript bloggers, and has been publishing a new post every day for years. Each one is bite-sized and easy to digest.",
                        description:"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.",
                        subjects : 'javascript',
                        img:'0'
                    },
                    {
                        title:"Ryan Chandler's Blog",
                        des:"Ryan writes about Laravel, PHP, and working with JavaScript, especially Alpine.js.",
                        description:"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.",
                        subjects : 'php',
                        img:'1'
                    },
                    {
                        title:"Aman Mittal's Blog",
                        des:"Aman often write posts on React.js, React Native and Node.js. These days his focus is on React Native and how to use it for cross-platform mobile development.",
                        description:"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.",
                        subjects : 'css',
                        img:'2'
                    },
                    {
                        title:"Daniel Copes' Blog",
                        des:"JavaScript and Web Development Tutorials. Flavio is one of the most recognizable JavaScript bloggers, and has been publishing a new post every day for years. Each one is bite-sized and easy to digest.",
                        description:"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.",
                        subjects : 'react',
                        img:'0'
                    },
                    {
                        title:"Sara Chandler's Blog",
                        des:"Ryan writes about Laravel, PHP, and working with JavaScript, especially Alpine.js.",
                        description:"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.",
                        subjects : 'php',
                        img:'2'
                    },
                    {
                        title:"Sahar Mittal's Blog",
                        des:"Aman often write posts on React.js, React Native and Node.js. These days his focus is on React Native and how to use it for cross-platform mobile development.",
                        description:"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.",
                        subjects : 'react.js',
                        img:'1'
                    },
                    {
                        title:"Aman Mittal's Blog",
                        des:"Aman often write posts on React.js, React Native and Node.js. These days his focus is on React Native and how to use it for cross-platform mobile development.",
                        description:"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.",
                        subjects : 'API',
                        img:'2'
                    },
                    {
                        title:"Daniel Copes' Blog",
                        des:"JavaScript and Web Development Tutorials. Flavio is one of the most recognizable JavaScript bloggers, and has been publishing a new post every day for years. Each one is bite-sized and easy to digest.",
                        description:"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi distinctio laudantium corporis optio incidunt vitae nam, dolorem nostrum numquam. Laudantium, nemo. Itaque iusto temporibus, nostrum quia cupiditate debitis error perspiciatis.",
                        subjects : 'git',
                        img:'0'
                    },
                ],
                show:false,
                seachWord: '',
            }
        },
        methods: {
            showBlog(blog){
                this.$emit('viewBlog',blog)
            }
        },
        mounted() {
            this.$emit('Blogs',this.blogs)
        },
        props:['filteredBlog','darkMode']
    }
</script>
<template>
    <div class="!grid gap-y-5">
        <div class="grid xs:grid-cols-1 sm:grid-cols-2 md:grid-cols-3 md:mt-20 xl:grid-cols-4 2xl:grid-cols-5 px-5 place-items-center mt-48 gap-y-10 justify-around w-full">
        <div  v-for="(blog) in filteredBlog" class="min-h-full container max-h-100 rounded-xl border-2 border-[#444] border-solid p-3 flex gap-y-3 flex-col justify-between md:w-72 xs:w-full sm:w-5/6 inline-block" :class="{'!border-[#314493]' : !darkMode}" :key=blog>

                <div class="poster rounded-lg overflow-hidden hover:opacity-80 duration-300 cursor-pointer">
                    <img @click="showBlog(blog)" class="w-full h-36" :src="`src/assets/img/${blog.img}.jpg`">
                    <!-- <img @click="showBlog(blog)" class="w-full h-40 object-cover hover:opacity-80 duration-300" :src="blog.img"> -->
                </div>
                <div class="text flex flex-col justify-between gap-y-1 sm:min-h-52">
                    <div class="content flex flex-col gap-y-2 ">
                        <h3 class="text-[#fff]" :class="{'text-[#000]' : !darkMode}">{{ blog.title }}</h3>
                        <p class="text-[#B8B8BE] text-sm hidden sm:block" :class="{'!text-[#000]' : !darkMode}">{{ blog.des }}</p>
                    </div>
                    <div  class="subjects">
                        <label class="text-sm bg-[#4b6bfb7c] text-[#fff] py-1 px-2 mr-2 rounded-md" :class="{'!bg-[#314493]' : !darkMode}">{{ blog.subjects }}</label>
                    </div>
                </div>
                <div class="container-submit">
                    <button class="bg-[transparent] text-[#4b6bfb7c] border-2 border-solid border-[#4b6bfb7c] w-full rounded-md py-1 text-base duration-300 hover:bg-[#4b6bfb7c] hover:text-[#fff]" @click="showBlog(blog)"  :class="{'!border-[#314493]' : !darkMode,'!text-[#314493]' : !darkMode}">veiw</button>
                </div>

        </div>
    </div>
    </div>
</template>


<!-- <style>
    :root{
        --gray-color:#444;
        --light-blue-color:#4b6bfb7c;
        --light-color-op:#ffffff93;
        --p-color:#B8B8BE;
        --light-color:#fff;

    }
    main{
        padding: 20px 10px;
        width: 100%;
        display: flex;
        flex-direction: column;
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
    .container-content{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 100%;

    }
    .container h3{
        color: var(--light-color);
        letter-spacing: 1px;
        font-weight: 400;
    }
    .container p{
        color: var(--p-color);
    }
    .subjects{
        display: flex;
        column-gap: 10px;
    }
    .container button{
        border: 1px solid var(--light-blue-color);
        color: var(--light-blue-color);
        border-radius: 10px;
        transition: 0.4s;
        background-color: transparent;
        cursor: pointer;
        padding: 8px;
        width: 100%;
        text-transform: capitalize;
        font-size: 0.9rem;
    }
    .container button:hover{
        background-color: var(--light-blue-color);
        color: var(--light-color);
    }
    .subjects label{
        background-color: var(--light-blue-color);
        padding: 3px 5px;
        border-radius: 5px;
        border: none;
        color: var(--light-color);
        font-size: 0.8rem;
        letter-spacing: 1px;
        transition: 0.4s;
    }
    .subjects label:hover{
        color: var(--light-color);
        cursor: pointer;
    }
    @media screen and (min-width:700px) {
        main{
            flex-direction: row;
        }
        .container{
            width: 300px;
        }

    }
</style> -->