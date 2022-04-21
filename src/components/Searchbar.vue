<template>
<div class="search">
    <div class="controllers">
    <p>{{ myjson.length }}  results found</p>
    <div class="show-buttons"><i class="far fa-th-large"></i><i class="fas fa-list"></i></div>
    <div class="dropdown"><span>Featured</span><div class="dropdown-content">
      <p>Lowest</p><br>
      <p>Highest</p></div></div>

    </div>
    <input type="text" placeholder="Search Product" v-model="search">

</div>
</template>


<script>
import json from "./products.json"

export default {
    
        data(){return {
          myjson:json,
           search: ""
           

        }},
         computed:{
    filteredProducts() {
      return this.myjson.filter(p => {
        // return true if the product should be visible

        // in this example we just check if the search string
        // is a substring of the product name (case insensitive)
        return p.name.toLowerCase().indexOf(this.search.toLowerCase()) != -1;
      });
    }
  }
        
    
  
 
    }

</script>

<style>
.controllers i{
  color: #7367f0;
}
.controllers{
  width:98%;
}
.dropdown{
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.18), 0 1px 10px 0 rgba(0, 0, 0, 0.18); 
  padding: 5px;
  border-radius: 10px;
  background-color: white;
  border: 1px solid #7367f0;
  color:#7367f0;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  display: inline-block;
  float: right;
}
.dropdown-content {
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.18), 0 1px 10px 0 rgba(0, 0, 0, 0.18);
  padding: 10px;
  background-color:white;
  display: none;
  position: absolute;
  z-index: 5;
}
.dropdown:hover .dropdown-content {
  display: block;
}

.show-buttons{
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  float: right;
}
.search p{
  display: inline-block;
  margin-left: 15px;

}
.search input{
  margin-left: 15px;
  border: none;
  padding: 14px;
  width: 95%;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.18), 0 1px 10px 0 rgba(0, 0, 0, 0.18);
  border-radius: 8px;
  margin-top: 12px;
  margin-bottom: 12px;
  background-color: rgb(255, 255, 255);
}
</style>