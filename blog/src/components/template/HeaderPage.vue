<template>
  <nav class="flex bg-[#fff] items-center justify-around flex-wrap fixed z-10 w-full" :class="{'!bg-[#040619]' : !darkMode}">
    <div class="pl-3 flex items-center gap-x-2 px-5 mt-3" >
      <img class="w-8 h-8" src="../../assets/img/icons8-blog-50-black.png" :class="{'hidden' : !darkMode}">
      <img class="w-8 h-8" src="../../assets/img/icons8-blog-50-white.png" :class="{'hidden' : darkMode}">
      <div @click="dayMode" class="container transition duration-500 theme-button border-solid border-3 border-red w-16 relative bg-[#000] h-8 rounded-full flex items-center ">
           <span @click="toggleDarkLight" class="transition-all duration-[400ms] ease-linear absolute cursor-pointer bg-cover sun w-6 h-6"></span>
        </div>
    </div>
    <div class="search py-4 my-1 flex justify-center px-5 mx-auto gap-x-2">
      <div class="flex relative items-center">
      <img class="absolute w-5 h-5 left-2" src="../../assets/img/icons8-search-64.png" alt="">
      <input v-model="searchWord" @keyup="searchBlog" @keyup.enter="searchBlog" class="w-full rounded-xl text-xs px-7 py-1.5 bg-[#000] opacity-20 text-[#fff]" :class="{'!bg-[#fff]': !darkMode, '!opacity-100' : !darkMode , '!text-[#000]': !darkMode}" type="text" placeholder="type here ...">
      </div>
      <button @click="searchBlog" class="border-none bg-[#314493] text-[#fff] px-2 py-py rounded-xl text-xs" :class="{'bg-[#314493]' : !darkMode}">search</button>
    </div>
    <div class="header-subjects xs:w-full md:w-1/3 flex px-5 justify-evenly flex-wrap gap-y-2 mb-2">
        <span @click="showSubjects" class="text-xs bg-[#314493] text-[#fff] py-1 px-2 rounded-md" v-for="blog in mainBlogs" :key="blog" :class="{'bg-[#314493]' : !darkMode}">{{ blog.subjects }} </span>
    </div>
  </nav>
</template>

<script>
export default {
  props: ['mainBlogs','darkMode'],
  data () {
    return {
    seachWord: '',
    darkisOn:true,
    }
  },
  methods: {
    searchBlog() {
      this.$emit('search',this.searchWord,'title')
    },
    showSubjects(e) {
      console.log(e.target.textContent);
      this.$emit('searchSubject',e.target.textContent,'subjects')
    },
    dayMode(){
      this.$emit('dark')
    },
    toggleDarkLight(){
      const icon= document.querySelector('.sun')
      icon.classList.toggle('moon')
      const container = document.querySelector('.container')
      container.classList.toggle('bg-[#fff]')
    }
  }

}
</script>

<style>
  .sun{
    background-image: url(../../assets/img/icons8-sun-30.png);
    left: 50%;
  }
  .moon{
    background-image: url(../../assets/img/icons8-moon-50.png);
    left:10%;
  }
</style>