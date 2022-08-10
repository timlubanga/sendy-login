<template>
  <div class="main">
    <div class="sector sector_left">
        <h1>
        We help you grow and do more
    </h1>

    <p class="para1">
        We bring together everything that’s required for E-commerce and Consumer 
        brands to ship goods to consumers and retailers across Africa. 
        It’s our mission to make trade easier.
    </p>

    <button>WATCH VIDEO</button>

    </div>

    <div class="sector sector_right">
    <div class="block-1">
        <img  class="image-1" src="https://assets-global.website-files.com/618ac079e7dd392826f282d6/61b08cc066c008000aae8d53_7.jpg" alt="image 1">
        <img  class="image-2" src="https://assets-global.website-files.com/618ac079e7dd392826f282d6/61b08cc706a5845fb27bf9f1_8.jpg" alt=" image 2">
    </div>
    <div class="block-2">
        <img  class="block-2-img image-3" src="https://assets-global.website-files.com/618ac079e7dd392826f282d6/61b08a2070a691176b24512b_4.jpg" alt=" image 3">
        <img  class=" block-2-img image-4" src="https://assets-global.website-files.com/618ac079e7dd392826f282d6/62e3df5193a3f85f2eb78b8b_Rectangle%2011.png" alt=" iamge 4">
        </div>
    </div>
    
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.main{
    display: flex;
    width: 60%;
    align-content: center;
    justify-content: space-around;
}


.sector{
    width:50%
}


.sector_right{
    display: flex;
    margin-left:10px;
    flex-direction: column;
    justify-content: center;
}



img {
    width: 140px;
    height: 138px;
    margin: 10px;
    border-radius: 5px;
}

.block-1{
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
}

.block-2{
    display: flex;
    justify-content: flex-end;
}


.block-2-img{
    width:50%
}
.image-2{
    height: 200px;
    width:150px;
}
h1{
    color:#17224d;
    font-size: 52px;
    padding-top:20px;
    padding-bottom: 10px;
    line-height:60px;
    font-weight: 400;
}


.para1 {
    width: auto;
    padding-top: 10px;
    color:#17224d;
    line-height: 35px;
    padding-bottom: 31px;
    font-family: Nunito,sans-serif;
    font-size: 21px;
    font-weight: 400;
}

button{
    background-color: #17224d;
    color: white;
    padding: 20px;
    padding-left:40px;
    font-size: 12px;
    text-align: center;
    padding-right: 40px;
    border-radius: 5px;
    border:none;
    outline: none;
}

button:hover{
    background: orange;
}


@media screen and (max-width: 1500px) {
  .main{
    flex-direction: column;
  }
}


@media screen and (max-width: 900px) {
    h1{
    font-size: 26px;
    padding-top:10px;
    padding-bottom: 5px;
    line-height:30px;
    font-weight: 300;
}

  
}

@media screen and (max-width: 1000px) {
    img {
    width: 100px;
    height: 160px;
    margin: 10px;
    border-radius: 5px;
}

.main{
    width: 100%;

}

.block-2-img{
    width:100%
}


.para1 {
   
    line-height: 25px;
    padding-bottom: 31px;
    font-family: Nunito,sans-serif;
    font-size: 16px;
    font-weight: 300;
}

.sector{
    width:100%
}

   

}


@media screen and (max-width: 521px) {

   img {
    width: 70px;
    height: 100px;
    margin: 10px;
    border-radius: 5px;
}

.image-2{
    height: 150x;
    width:150px;
}

.image-1{
    height: 150x;
    width:100px;
}

 
}


@media screen and (max-width: 350px) {

   img {
    width: 40px;
    height: 50px;
    margin: 5px;
    border-radius: 5px;
}

.image-2{
    height: 150px;
    width:100px;
}

.image-1{
    height: 80px;
    width:70px;
}

 
}


</style>