<template>
<div>
  <div class="home">
    <MainSector/>
    
  </div>
  <div class=footer>
      <h1>
        A fully integrated suite of distribution products.
      </h1>
    </div>
</div>
</template>

<script>


import MainSector from "../components/MainSector.vue"
export default {
  name: 'HomeView',
  components:{MainSector}
  
}
</script>

<style scoped>
.home{
  display:flex;
  justify-content: center;
  margin-top:30px;
}


.footer{
  margin-top: 30px;
  background-color: rgb(238, 245, 248);
  padding:40px;
  
}

h1{
  font-size: 24px;
  font-weight: 700;
}
</style>
