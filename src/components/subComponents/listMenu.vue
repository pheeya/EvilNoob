<template>
<div class="main">
     <div><img id="three" v-on:click="showList=true"
     src="https://c.s-microsoft.com/en-us/CMSImages/icon_menu_new.png?version=2e17c0b9-dc99-1d59-c64d-0be30696e854"> 
  </div>
     <div v-if="showList" class="overlay"></div>
    <transition name="slide">
    <div v-if="showList" class="main">
        
    
           
          
          
            <div  class="back">
            
        <ul>
            <li id="imgSRC"><img src="https://js.pngtree.com/v2/images/pngtree_logo.png" alt=""> </li>
  <img v-on:click="showList=false" id="x" src="https://docs.updatefactory.io/images/close-x.png" alt="">
            <li>GAMES</li>
            <li>SHOP</li>
            <li>NEWS</li>
            <li>ESPORTS</li>
            
            
         
            <li>My Account</li>
            <li>Support</li>
        </ul>
        </div>
    </div></transition>
    </div>
</template>

<script>
export default {
    data: function ()
    {
       return{ showList:false}
    },



}
</script>

<style scoped>

.overlay 
{
    width:100vw;
    height:100vh;
    background:rgba(19, 14, 14, 0.575);
    position: fixed;
}
#three
{
position:absolute;
width:35px;
top:15px;
left:10px;
cursor:pointer;
}
#x 
{
    position: absolute;
    width:20px;
    top:15px;
    left:10px;
    cursor: pointer;
}

.slide-enter 
{

}

.slide-enter-active
{
   animation: slide-in .3s;
    
}


.slide-leave-to
{
    animation: slide-out .3s;
}
@keyframes slide-in 
{
    from{
        transform: translateX(-100%);

    }
    to {
        transform: translateX(0)
    }
}

@keyframes slide-out 
{
    from {
        transform: translateX(0);
    }
    to 
    {
        transform: translateX(-100%);
    }
}

#imgSRC 
{
 height:50px;   

}

#imgSRC img 
{
    position: absolute;
    width:200px;
    top:0;
    left:60px;

}
.main 
{
   
    position:absolute;
    z-index:101;
      font-family: 'Montserrat', sans-serif;
      display:none;
      top:0;
      padding:0;
      margin:0;
     font-size:16px;
      
      width:330px;
      font-weight:500;
}

.back 
{
      background-color: #121a22;
      width:350px;
   position:fixed;
      height:100vh;
}
.back ul 
{
    list-style-type:none;
    color:white;

   text-align:left;
   padding:0;
   margin:0;
   display:flex;
   flex-direction:column;
 
}
.back ul li 
{

  border-top:.5px solid rgba(179, 177, 177, 0.74);

   
margin-left:0;
cursor: pointer;

padding:15px;
transition: all .2s;
 color:rgba(201, 201, 201, 0.87);
}
ul li:hover 
{
   color:white;
}

@media (max-width:870px)
{
    .main 
    {
        display:block;
    }
}
</style>
