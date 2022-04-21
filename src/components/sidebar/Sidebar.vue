 <template>
     <div class="sidebar" :id="width">
        <div class="header">

            <div class="logo" :class="{closed : toggler}">
             <span class="brand-logo">
                <img src="https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/logo.36f34a9f.svg" alt="">
             </span>
             <h2>Vuexy</h2>
            </div>

            <div class="expand">
             <a @click="toggleS"><svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="t-button"><circle cx="12" cy="12" r="10"></circle><circle cx="12" cy="12" r="3"></circle></svg> </a>
            </div>

        </div>
        <div class="sidebar-container" id="sbar" :class="{closed : toggler}">
         <ul>
            <li v-for="item in items" class="sbar-item"> {{ item }} </li> 
         </ul>
        </div>
 </div>
 </template>

<script>
export default {
     data(){
         return{
             toggler: true,
             width: true,
             items:["Email" , "Chat" , "Todo" , "Calendar" , "Invoice" , "eCommerce" , "User" , "Pages"]
             
         }
     },
     methods:{
         toggleS(){
             this.width = !this.width
             this.toggler = !this.toggler
         }

     }
     
 }
 </script>

<style scoped>
#true{
    width: 55px;
}
.closed {
 display: none;
}
.t-button{
    cursor: pointer;
    vertical-align: middle;
}
.logo h2{
    color: #7367f0;
    font-weight: 600;
    letter-spacing: .01rem;
    font-size: 1.45rem;
    padding-left: 1rem;
    vertical-align: middle;
    margin-top: 0px;
    margin-bottom: 0px;
}
.brand-logo img{
    max-width: 36px;
    border-style: none;
    vertical-align: middle;
    color: #7367f0;

}

.brand-logo{
    color: #7367f0;

}
.header{
    display: flex;
    padding: .35rem 1rem .3rem 1.14rem;
    width: 233px;
    height: 4.45rem;
    position: relative;
    color: #6e6b7b;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.45;
    letter-spacing: .01rem;
}
.logo{
    width: 260px;
    height: 4.45rem;
    position: relative;
    color: #6e6b7b;
}
.sbar-item{
    padding: 10px 15px 10px 15px;
    margin: 0 15px;
    color: #625f6e;
    line-height: 1.45;
    text-overflow: ellipsis;
    overflow: hidden;
    outline: none;
    background-color: transparent;
    align-items: center;
    display: flex;
    box-sizing: border-box;
    text-decoration: none;
    position: relative;
    white-space: nowrap;
    font-size: 0.99rem;
    font-family: Montserrat,Helvetica,Arial,serif;
    font-weight: 400;
    overflow-y: hidden;
    letter-spacing: .01rem;
    cursor: pointer;
    transition: 0.3s;
}
.sbar-item:hover{
    transform: translateX(6px);
}
.sidebar-container{
    transition: 0.5s;
}
.sidebar{
    background: #fff;
    display: flex;
    flex-direction: column;
    padding-bottom: .75rem;
    overflow-x: hidden;
    margin: 0px;
    padding: 0px;
    color: #6e6b7b;
    height: calc(100% - 4.45rem);
    position: relative;
    box-shadow: 0 0 15px 0 rgb(34 41 47 / 5%);
    width: 260px;
    }
.sidebar li{
    list-style: none;
}
 
 </style>
 
