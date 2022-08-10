<template>
  <div class="order">
   
    <form >
  <div class="container">
    <input type="text"  placeholder="Enter a pick up location" name="pick" required>
    <input type="text"  placeholder="Enter a destination location" name="des" required>

    <button>CONFIRM ORDER</button>
  </div>
</form>
  </div>
</template>

<script>
export default {
  name:"MakeOrder",

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
.order{
  display: flex;
  flex-direction: row;
  align-items:center;
  justify-content: flex-start;
  width: 100%;
  position: fixed;
  z-index: 1;
  left: -5%;
  overflow: auto;
  top: 15%;

  


}
form {
  display: flex;
  justify-content: center;
}

input[type=text]{
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  box-sizing: border-box;
}

button {
  background-color: rgb(136, 133, 133);
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  cursor: pointer;
  width: 100%;
}


button:hover {
  background-color: rgb(22, 79, 97);
}


.container {
  margin-top: 0px;
  margin-left:0px;
  padding: 30px;
  padding-top:0px;
  background: white;
  border: 1px solid #e6dcdc;
  width: 60%;
}

@media screen and (max-width: 480px) {
  .container {
    width:100%
  }
  .order{
    width:100%;
    left: 0;
  }
}



</style>