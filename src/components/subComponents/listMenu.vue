<template>
<div class="main">
     <div><img id="three" v-on:click="showList=true"
     src="https://cdn1.iconfinder.com/data/icons/social-messaging-ui-color/254000/30-512.png"> 
  </div>
     <div v-if="showList" class="overlay"></div>
    <transition name="slide">
    <div v-if="showList" class="main">
        
    
           
          
          
            <div  class="back">
            
        <ul>
            <li id="imgSRC"><img src="https://cdn.discordapp.com/attachments/584665267078955009/596189239620796436/logo.png" alt=""> </li>
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
    width:120vw;
    height:120vh;
    background:rgba(19, 14, 14, 0.575);
    position: fixed;
}
#three
{
position:absolute;
width:35px;
top:10px;
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
    width:150px;
    top:20px;
    left:90px;

}
.main 
{
   
    position:fixed;
    z-index:101;
      font-family: 'Montserrat', sans-serif;
      display:none;
      top:0;
      padding:0;
      margin:0;
     font-size:16px;
      
      width:330px;
      font-weight:500;
      height:120vh;
}

.back 
{
    height:120vh;
      background-color: #121a22;
      width:350px;
   position:absolute;
      height:100%;
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
