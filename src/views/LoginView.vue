<template>
  <div class="auth">
   
    <form >
  <div class="container">
    <input type="username" v-model="username"  placeholder="Enter Username" name="uname" required>
    <input type="password" v-model="password" placeholder="Enter Password" name="psw" required>

    <button type="submit" @click="submit">Login</button>
    <router-link  to="/login">Forgot password?</router-link>
  </div>
</form>
  </div>
</template>

<script>
export default {
  name:"LoginPage",
  data(){
    return {
      username:"",
      password:"",
      isAuthenticated:false,
    }
  },
  methods:{
    submit(){
      if (this.password=="admin" && this.username=="admin"){
        window.localStorage.setItem("isAuthenticated", true);
        alert("logged in successfully")
        this.$router.push('/orders')
        return
      }
      alert("wrong username or password")
    }

  }
}
</script>




<style scoped>
div a{
  text-decoration: none;
  color:rgb(63, 141, 167);
}

h3{
  color: gray;
  font-weight: 400;
  font-size: 20px;


}
.auth{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  


}
form {
  display: flex;
  justify-content: center;
}

input[type=username], input[type=password] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  box-sizing: border-box;
}

button {
  background-color: rgb(24, 151, 194);
  color: white;
  padding: 14px 20px;
  font-size: 18px;
  margin: 8px 0;
  border: none;
  cursor: pointer;
  width: 100%;
}


button:hover {
  background-color: rgb(22, 79, 97);
}


.container {
  margin-top: 40px;
  padding: 30px;
  border: 1px solid #e6dcdc;
  width: 60%;
}



</style>