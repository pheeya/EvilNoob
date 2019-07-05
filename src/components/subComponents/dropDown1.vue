<template>
    <transition name="fade"> <div v-if="showMenu" class="main">
<div class="menu">
<ul>
    <h3 style="margin:0;padding:10px; color:white; font-weight:200;">EvilNoobs</h3>
    <li><img src="/media/braverz-logo.png"><h4>GAME1</h4></li>
    <li><img src="/media/braverz-logo.png"><h4>GAME2</h4></li>
    <li><img src="/media/braverz-logo.png"><h4>GAME3</h4>  </li>
    <li><img src="/media/braverz-logo.png">  <h4>GAME4</h4></li>
    <li><img src="/media/braverz-logo.png"><h4>GAME5</h4></li>
 

</ul>

<div class="footer">
<ul>
    <li>More Games</li>
    <li>Downloads</li>
    <li>Game Forums</li>
</ul>

</div>


</div>


    </div></transition>
</template>

<script>
export default {
   
        
         props:['showMenu']
     
   

}
</script>

<style scoped>

h4  
{
    text-align:center;
    margin:0;
}
.fade-enter 
{
    opacity:0;
}

.fade-enter-active 
{
    transition:opacity .4s;
    animation:slide-in .4s;
}

.fade-leave 
{
    opacity:1;
}
.fade-leave-active 
{
        animation:slide-out .4s;


}

.fade-leave-to 
{
    transition:opacity .4s;
    opacity:0;
}

@keyframes slide-in 
{
    from{transform:translateX(-100%)}
    to{transform: translateX(0)}
}

@keyframes slide-out 
{
    from{transform: translateX(0)}
    to {transform: translateX(-100%)}
}


.main 
{
      font-family: 'Montserrat', sans-serif;
    position: absolute;
z-index:99999999999999999999;
width:100%;
}
.menu ul 
{
    list-style-type:none;
    padding:0;
    margin:0;
    width:100%;
    text-align:center;
}
.menu 
{
    width:100%;
    box-sizing: border-box;
    background-color: #0d1825f3;
  text-align:left;
 
}
li img 
{
    width:120px;
    cursor:pointer;
}
ul li 
{
    display:inline-block;
    margin:5px;
   text-align:center;
    color:white;
    padding:30px 0;
    margin-right:50px;
}

.footer ul 
{
    text-align:center;
  margin:0;
  padding:10px 0;
     border-top:1px solid rgba(114, 114, 114, 0.795);
}
.footer ul li 
{
    padding:0;
    margin:5px 20px;
    cursor:pointer;
 
}


@media (max-width:870px)
{
    .main
    {
        display:none;
    }
}

</style>
