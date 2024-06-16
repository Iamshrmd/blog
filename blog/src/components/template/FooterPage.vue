<template>
    <div class="footer-bg w-full">
      <div class="footer-wave w-full h-52 relative mt-7 ">

      <svg class="absolute -bottom-4 -z-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path :fill="darkMode ? '#fff' : '#040619'" fill-opacity="1" d="M0,224L60,197.3C120,171,240,117,360,85.3C480,53,600,43,720,64C840,85,960,139,1080,138.7C1200,139,1320,85,1380,58.7L1440,32L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path></svg>
      </div>
      <div class="footer-items py-5 flex flex-col bg-[#fff] px-5 gap-y-10 gap-x-10 z-2" :class="{'!bg-[#040619]' : !darkMode}">
        <div class="footer-links grid xs:grid-cols-1 sm:grid-cols-2 md:grid-cols-4 items-center justify-evenly px-2  gap-y-3">
            <ul class="link flex items-center justify-center flex-col">
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
            </ul>
            <ul class="link flex items-center justify-center flex-col">
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
            </ul>
            <ul class="link flex items-center justify-center flex-col">
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
            </ul>
            <ul class="link flex items-center justify-center flex-col">
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
              <li><a class="text-[#040619]"  :class="{'!text-[#fff]' : !darkMode}" href="#">link</a></li>
              </ul>
        </div>
            <div class="footer-icons flex gap-y-3 justify-evenly">
            <div class="flex justify-center items-center">
            <img class="w-9 h-9" src="../../assets/img/icons8-instagram-50.png"  :class="{'hidden' : !darkMode}">
            <img class="w-9 h-9" src="../../assets/img/icons8-instagram-50 (1).png" :class="{'hidden' : darkMode}">
            </div>
          <div class="flex justify-center items-center">
            <img class="w-9 h-9" src="../../assets/img/icons8-linkedin-50.png"  :class="{'hidden' : !darkMode}">
            <img class="w-9 h-9" src="../../assets/img/icons8-linkedin-50 (1).png" :class="{'hidden' : darkMode}">
          </div>
          <div class="flex justify-center items-center">
            <img class="w-9 h-9" src="../../assets/img/icons8-telegram-50.png"  :class="{'hidden' : !darkMode}">
            <img class="w-9 h-9" src="../../assets/img/icons8-telegram-50 (1).png" :class="{'hidden' : darkMode}">
          </div>
          <div class="flex justify-center items-center">
            <img class="w-9 h-9" src="../../assets/img/icons8-twitter-50.png"  :class="{'hidden' : !darkMode}">
            <img class="w-9 h-9" src="../../assets/img/icons8-twitter-50 (1).png" :class="{'hidden' : darkMode}">
          </div>
        </div>
      </div>

    </div>
</template>

<script>
export default {
  props: ['darkMode']
}
</script>

<style>
</style>