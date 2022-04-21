<template>
<div class="side">
    <p>Filters</p>
<div class="card f" id="f">
    <div class="price-group flex-column">
        <h3>Multi Range</h3>
        <div class="radio">
            
        </div>
        <div class="radio">
        <input type="radio" name="1" id="">
        <label for="1"><span>All</span></label>

        </div>
        <div class="radio">
        <input type="radio" name="2" id="">
        <label for="2"><span> = $10</span></label>

        </div>
        <div class="radio">
        <input type="radio" name="3" id="">
        <label for="3"><span>$10 - $100</span></label>

        </div>
        
        <div class="radio">
        <input type="radio" name="4" id="">

        <label for="4"><span>$100 - $500</span></label>
        </div>
        <div class="radio">
        <input type="radio" name="5" id="">
        <label for="5"><span>= $500</span></label>

        </div>
    </div>

    <div class="price-range flex-column">
        <input type="range" name="" id="">
    </div>
    <div class="cat flex-column">
    <h4>Categories</h4>
    <div class="radio">
        
    <input type="radio" name="6" id="">
    <label for="6">Car</label>
    </div>
    <div class="radio">
    <input type="radio" name="7" id="">
    <label for="7">Audio</label>

    </div>
    <div class="radio">
    <input type="radio" name="8" id="">
    <label for="8">Camera</label>

    </div>
    <div class="radio">
    <input type="radio" name="9" id="">
    <label for="9">Phone</label>

    </div>
    <div class="radio">
    <input type="radio" name="10" id="">
    <label for="10">Computer</label>

    </div>
    <div class="radio">
    <input type="radio" name="11" id="">
    <label for="11">Tablets</label>

    </div>
    <div class="radio">
    <input type="radio" name="12" id="">
    <label for="12">Health</label>

    </div>
    <div class="radio">
    <input type="radio" name="13" id="">
    <label for="13">TV</label>

    </div>
    <div class="radio">
    <input type="radio" name="14" id="">
    <label for="14">Home</label>

    </div>
    <div class="radio">
    <input type="radio" name="15" id="">
    <label for="15">Accessories</label>

    </div>
    </div>
    <div class="brands flex-column">
    <h4>Brands</h4>
    <div class="radio">
        
    <input type="radio" name="6" id="">
    <label for="6">Samsung</label>
    </div>
    <div class="radio">
        
    <input type="radio" name="6" id="">
    <label for="6">Metra</label>
    </div>
    <div class="radio">
        
    <input type="radio" name="6" id="">
    <label for="6">HP</label>
    </div>
    <div class="radio">
        
    <input type="radio" name="6" id="">
    <label for="6">Apple</label>
    </div>
    <div class="radio">
        
    <input type="radio" name="6" id="">
    <label for="6">GE</label>
    </div>
    <div class="radio">
        
    <input type="radio" name="6" id="">
    <label for="6">Sony</label>
    </div>
    <div class="radio">
        
    <input type="radio" name="6" id="">
    <label for="6">Whirlpool</label>
    </div>
    <div class="radio">
        
    <input type="radio" name="6" id="">
    <label for="6">KitchenAid</label>
    </div>
    
    <div class="rates flex-column">
        <h4>Ratings</h4>
        <a href="#"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>&up</a>
        <a href="#"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="far fa-star"></i>&up</a>
        <a href="#"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i>&up</a>
        <a href="#"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i>&up</a>
        <a href="#"><i class="fas fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i>&up</a>
    </div>
    </div>
</div>

</div>

</template>

<style>
.side p{
    margin-left: 16px;
}
.rates{
    text-decoration: none;
}
#f{
   margin-right: 7rem;
   display: flex;
   flex-direction: column;
}
.flex-column{
    display: flex;
    flex-direction: column;
}

.f{
    
    padding: 5px;
    display: flex;
    flex-direction: column;
    width: 90%;
}
.radio{
    padding-bottom: 5px;
    color: black;
}
</style>
