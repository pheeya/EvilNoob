<template>
    <transition name="slide">
    <div v-if="listMenu" class="main">
        
         
           
          
          
            <div  class="back">
            
        <ul>
            <li>GAMES</li>
            <li>SHOP</li>
            <li>NEWS</li>
            <li>ESPORTS</li>
            
            
         
            <li>My Account</li>
            <li>Support</li>
        </ul>
        </div>
    </div></transition>
</template>

<script>
export default {
props:['listMenu']
}
</script>

<style scoped>


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

.main 
{
    position:absolute;
    z-index:100;
      font-family: 'Montserrat', sans-serif;
      display:none;
}

.back 
{
      background-color: #1a1d20f5;
      margin-top:-10px;
      width:50vw;
      height:100vh;
}
.back ul 
{
    list-style-type:none;
    color:white;
    margin:60px 10px;
   text-align:left;
   padding:0;
   padding-top:10px;
   display:flex;
   flex-direction:column;
}
.back ul li 
{

  
    border-top:.1px solid rgba(255, 255, 255, 0.479);
    border-bottom:.1px solid rgba(255, 255, 255, 0.267);
margin-left:0;
cursor: pointer;
width:200px;
padding:20px;
transition: all .3s;

}
ul li:hover 
{
    background-color:rgba(94, 94, 94, 0.801);
}

@media (max-width:870px)
{
    .main 
    {
        display:block;
    }
}
</style>
