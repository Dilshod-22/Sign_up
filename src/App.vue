<template>
  <div class="home h-screen w-full flex items-center justify-center bg-white">
    <div class="h-96 w-[1200px] relative bg-[rgb(0,0,0,.7)] grid grid-cols-2 text-white">
      <div class="flex items-center justify-center">
        <div class="h-52 w-96">
          <h2 class="text-2xl font-medium">Don't have an acoount?</h2>
          <p class="w-80 h-24 mt-3">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
          <button class="login h-10 w-24 rounded-3xl" @click="login">SIGN UP</button>
        </div>
      </div>
      <div class="flex items-center justify-center">
        <div class="h-52 w-96">
          <h2 class="text-2xl font-medium">Have an account?</h2>
          <p class="w-80 h-20 mt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore, aspernatur.</p>
          <button class="login h-10 w-24 rounded-3xl" @click="login">LOGIN</button>
        </div>
      </div>
      <div class="page absolute h-[430px] w-[420px] bg-white rounded-lg" :class="[ loginPage ? ['left-[650px]'] : 'left-[100px]']" >
        <div class="py-28 px-20 signPage" :class="[ show ? 'opacity-100' : 'opacity-0']" v-if="loginPage">
          <h2 class="text-2xl font-medium text-black">login</h2>
          <form action="" @submit.prevent>
            <input class="mt-5 shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Username"> 
            <input class="mt-3 shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Password"> 
            <button class="bg-cyan-400 text-white h-10 w-20 mt-8 rounded-2xl" type="submit">Login</button>
            <a href="Forget?"></a>
          </form>
        </div>
        <div class="py-20 px-20 signPage" :class="[ show ? 'opacity-0' : 'opacity-100']" v-else>
          <h2 class="text-2xl font-medium text-black">Sign Up</h2>
          <form action="" @submit.prevent>
            <input class="mt-5 shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Full name"> 
            <input class="mt-5 shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Email"> 
            <input class="mt-3 shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Password"> 
            <button class="bg-cyan-400 text-white h-10 w-20 mt-8 rounded-2xl" type="submit">Sign Up</button>
            <a href="Forget?"></a>
          </form>
        </div>
    </div>
    </div>
  </div>
</template>

<script >
  export default {
    data(){
      return{
        loginPage:true,
        show:true,
      }
    },
    methods:{
      login(){
        setTimeout(() => {
          this.show = !this.show          
        }, 500);
        this.loginPage = !this.loginPage          
      }
    }
  }
</script>

<style scoped>
.home{
  background-image: url("./image/the-old-vintage-black-brick-wall-background-with-lighting-decoration-and-dark-tone-style-for-background-design-concept-free-photo.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
.login {
  border:1px solid lime;
}
.page{
  transition: 1s;
  margin-top:-25px;
}
.signPage{
  transition: 1s;
}
</style>