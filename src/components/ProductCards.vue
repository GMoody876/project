<template>
<div class="container">
    
    <div class="top">
        <h2>Shop    </h2>
        <span>

        <h4><i class="fas fa-home"></i> > ECommerce  > </h4>
        </span>
        <h4>Shop</h4>
    </div>
    <div class="wrapper">
    
    <div class="filter">
        <Filterbar />
    </div>
    <div class="search-and-cards">
        <Searchbar />
    <div class="flex-c" id="flex-c">
        <div class="card i" v-for="data in myjson">
            <div class="pic"><img :src="data.img" alt=""></div>

            <div class="price-rate-cont pad">
            <div class="price-rating"><p v-for="i in data.rating" id="rate"><i class="fas fa-star"></i></p>

            </div>

            <p id="price">{{ data.price + "$" }}</p></div>
            <div class="product-name pad">{{ data.name }}</div>
            <div class="details pad">On Retina display that never sleeps...</div>
            <div class="btns">
            <button class="fav">Wishlist</button>
            <button class="cart">View in Cart</button>
            </div>
        </div>
    </div>

    </div>
    

    </div>
    
</div>
</template>


<script>
import Filterbar from'./Filterbar.vue'
import Searchbar from './Searchbar.vue'
import json from "./products.json"


export default {
    components:{ Searchbar , Filterbar },

    data(){
        return{
            myjson: json,
            
    }
  },
  computed:{
      
      
      
  }
  

        }
</script>
<style >
.i{
    transition: 0.5s;
}
.i:hover{
    transform: translateY(-8px);
    box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.30), 0 1px 10px 0 rgba(0, 0, 0, 0.30);
}
.details{
    font-size: 0.75rem;
    margin-top: 0.28rem;
    padding-bottom: 10px;
}
.pad{
    padding-left: 1em;
    padding-right: 1em;

}
.wrapper{
    display: flex;
    align-items:flex-start;

}
.cart{
    cursor: pointer;
    padding-top: 0.786rem;
    padding-right: 1.5rem;
    padding-bottom: 0.786rem;
    padding-left: 1.5rem;
    border: none;
    background-color:#7367f0;
    color:white;
    font-family:'Montserrat', sans-serif;
    font-size: 1rem;
    font-weight: 500;

}
.fav{
    font-weight: 500;
    cursor: pointer;
    background-color: #f6f6f6;
    padding-top: 0.786rem;
    padding-right: 1.5rem;
    padding-bottom: 0.786rem;
    padding-left: 1.5rem;
    border: none;
    font-family:'Montserrat', sans-serif;
    font-size: 1rem;

}
.btns{
   
    display: flex;
    flex-direction: column;
    align-self: flex-end;
    width: 100%;
    position: relative;
}
.product-name{
    max-width: 21rem;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    font-size: 0.95rem;
    font-weight: bold;
}
.flex-c{
    width: 100%;
    box-sizing: border-box;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    column-gap: 2rem;
}
.container{
    
    margin: 10px;
}

h2 , h4 {
    display: inline;
}
.card{
    box-sizing: border-box;
    overflow: hidden;
    margin: 1rem;
    margin-bottom: 2rem;
    box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.18), 0 1px 10px 0 rgba(0, 0, 0, 0.18);
    border-radius: .428rem;
    background-color: #fff;
    background-clip: border-box;
    position: relative;
    display: flex;
    flex-direction: column;
    min-width: 0;
    word-wrap: break-word;
    border: none;
}
.pic{
    background-color: transparent;
    color: #7367f0;
    text-decoration: none;
    box-sizing: border-box;
    cursor: pointer;
    text-align: center;
    display: flex;
    align-items: center;
    
}
.pic img{
    display: flex;
    flex-shrink: 0;
    max-width: 100%;
    height: auto;
    width: 100%;
    vertical-align: middle;
    box-sizing: border-box;
}
.price-rate-cont{
    display: flex;
    justify-content: space-between;
    align-items: baseline;
}
.price-rating{
    margin: ;
    display: flex;
    align-items: baseline;

}
.top span{
    color:#7367f0;
}
 .top{
    margin-bottom: 20px;
    margin-left: 16px;
    margin-top: 100px;
}
#rate{
    display: flex;
    justify-content: baseline;

}
</style>