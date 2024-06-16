<script>
  import BlogPage from './components/BlogPage.vue';
  import ViewBlog from './components/ViewBlog.vue';
  import HeaderPage from './components/template/HeaderPage.vue';
import FooterPage from './components/template/FooterPage.vue';
  export default {
    components: {BlogPage, ViewBlog, HeaderPage, FooterPage},
    data() {
      return {
        showView:false,
        showPage:true,
        selectedBlog: null,
        filteredBlog: null,
        mainBlogs: null,
        showNotFounded : false,
        darkMode:true
      }
    },
    methods: {
      viewblog(blog) {
        this.selectedBlog=blog
        this.changePage1()
      },
      changePage1(){
        this.showView=true;
        this.showPage=false;

      },
      changePage2(){
        this.showView=false;
        this.showPage=true;

      },
      searchBlog(searchWord) {
        this.showNotFounded=false
                if (!searchWord) {
                  this.filteredBlog = this.mainBlogs.filter(b => {
                    return b
                  })
                }
                this.filteredBlog = this.mainBlogs.filter(b => {
                    if (b.title.toLowerCase().includes(searchWord.toLowerCase())) return b
                })
                if(this.filteredBlog.length == 0 ){
                  this.showNotFounded=true;
                }
                },
                getBlogs(blogs){
                  this.filteredBlog = blogs
                  this.mainBlogs = blogs
                  console.log(this.mainBlogs);

      },
      searchSubjects(subjects) {
        this.showNotFounded=false
        this.filteredBlog = this.mainBlogs.filter(b => {
          if (b.subjects.toLowerCase().includes(subjects.toLowerCase())) return b
        })
        console.log(this.filteredBlog);
        if(this.filteredBlog.length == 0 ){
          this.showNotFounded=true;
        }
        },
        changeMode(){
          this.darkMode = !this.darkMode
        }
    },
    mounted(){
      this.filteredBlog=this.mainBlogs
    }
  }
</script>

<template>
  <div :class="{'bg-[#040619]' : darkMode}">
    <HeaderPage @search="searchBlog" :mainBlogs="mainBlogs" @searchSubject="searchSubjects" @dark="changeMode" :darkMode="darkMode"/>
    <main class="min-h-96">
      <div class="flex items-center justify-center h-96 w-full" v-if="showNotFounded">
        <p class="text-[#fff] text-center" :class="{'!text-[#000]' : !darkMode}">couldn't find your blog</p>
      </div>
      <BlogPage v-if="showPage" @viewBlog="viewblog" @search="searchBlog" @Blogs="getBlogs" :filteredBlog="filteredBlog"  :darkMode="darkMode">
      </BlogPage>
      <ViewBlog v-if="showView" @exit="changePage2" :blog="selectedBlog" :darkMode="darkMode"/>
    </main>
    <FooterPage :darkMode="darkMode"/>
  </div>
</template>

<style scoped>
*{
  margin: 0;
  padding: 0;
}
@media (min-width: 1024px) {
  /* header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  } */
}
</style>
