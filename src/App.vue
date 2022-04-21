<template>
<div class="flex-high-cont">
<div class="sidebarfloat">
  <Sidebar />
</div>
<div class="other-cont">
  <div class="navynav">
     <Navbar />
  </div>
  <div class="prods">
     <ProductCards />

  </div>

</div>

</div>

</template>
<script>

import Navbar from './components/Navbar.vue'
import ProductCards from './components/ProductCards.vue'
import Sidebar from './components/sidebar/Sidebar.vue'


export default {

  components: { Navbar , ProductCards , Sidebar },


  data() {
    return {
      title: 'Data binding'
    }
  },
  methods: {
    sayWow(){
      console.log("wow")
  },
}}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
h1, h2 ,h3 ,h4 , h5, h6{
    font-family: inherit;
    font-weight: 500;
    line-height: 1.2;
} 
.navynav{
  width: 80%;
}
body{
font-size: 1rem;
font-family: 'Montserrat', sans-serif;
color: #4b4b4b;
background-color: #f6f6f6;
}
.sidebarfloat{
  float:left;
}
.flex-high-cont{
  display: flex;
  flex-shrink: 0;
}
.other-cont{
  display: flex;
  flex-direction: column;
  }



</style>