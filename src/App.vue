<template>
  <nav>
    <div class="left-nav">
    <router-link v-if="['login', 'orders'].includes($route.name)" to="/"> <img class="image1" src="https://images.sendyit.com/web_platform/logo/rebrand_logo.png"></router-link>
    <router-link  v-else to="/"> <img class="image" src="https://assets-global.website-files.com/618ac079e7dd392826f282d6/618bbbc3ed9711ebf9fd0683_logo.svg"></router-link>  
    </div>
    <div class="right-nav">
    <router-link v-if="!['login', 'orders'].includes($route.name)"  to="/">Products </router-link>
    <router-link v-if="!['login', 'orders'].includes($route.name)" to="/"> About Us</router-link>
    <router-link v-if="!['login', 'orders'].includes($route.name)" to="/">Blog </router-link>
    <router-link v-if="!['login', 'orders'].includes($route.name)" to="/">Careers </router-link>
    <router-link v-if="!['login', 'orders'].includes($route.name)"  to="/">Contact Us </router-link>
    <router-link  v-if="!['login', 'orders'].includes($route.name)" class="login" to="/login">Login</router-link>
    <span  v-if="['orders'].includes($route.name)" @click="handleLogout" >Log out</span>
    </div>
  </nav>
  <router-view/>
</template>

<script>




export default {

  methods:{
    handleLogout(){
      window.localStorage.removeItem('isAuthenticated')
       this.$router.push('/login')

    },

    

  },
  
  
}
</script>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 16px;
  flex-direction: row;
  display: flex;
  justify-content:space-around;
  align-items: center;
  background-color: #1782c5;
  z-index: 9

}

.right-nav{
  display: flex;
  justify-content: space-around;
  width: 40%;
  align-items: center;
}

.left-nav{
  display: flex;
  align-items: center;
}


.image{
  width:30%;
  height:30%;
  ;
}


.image1{
  width:15%;
  height:15%;
  ;
}

.login{
  color: rgb(29, 35, 37);
  padding: 10px;
  padding-left:30px;
  padding-right: 30px;
  background: rgb(210, 156, 56);
  border-radius: 15px;
  text-decoration: none;

  
}


span{
  color: white;
}


span:hover{
  cursor: pointer;

}


nav a.router-link-exact-active {
  text-decoration:none;
  color: white;
}


@media screen and (max-width: 1200px) {
  .right-nav{
    width:80%
  }
}

@media screen and (max-width: 800px) {
  .left-nav{
    display: none;
  }
  .right-nav{
    font-size:12px;
  }
}

</style>
