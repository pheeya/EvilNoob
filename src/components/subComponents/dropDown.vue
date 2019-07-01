<template>
    <transition name="fade"> <div v-if="showMenu" class="main">
<div class="menu">
<ul>
    <h2 style="margin:0;padding:10px; color:white; font-weight:200;">EvilNoobs</h2>
    <li><img src="https://blznav.akamaized.net/img/games/logo-codbo4-7794ee86f3e8be3e.png"></li>
    <li><img src="https://blznav.akamaized.net/img/games/logo-dest2-db71def7c167da44.png"></li>
    <li><img src="https://blznav.akamaized.net/img/games/logo-heroes-78cae505b7a524fb.png">  </li>
    <li><img src="https://blznav.akamaized.net/img/games/logo-hs-93512467e87f82c6.png">  </li>
    <li><img src="https://blznav.akamaized.net/img/games/logo-codmw-d57b296321d6b444.png"></li>
 

</ul>
<hr>
<div class="footer">
<ul>
    <li>More Games</li>
    <li>Downloads</li>
    <li>Game Forums</li>
</ul>

</div>

<hr>
</div>


    </div></transition>
</template>

<script>
export default {
   
        
         props:['showMenu']
     
   

}
</script>

<style scoped>

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

hr 
{
    border:.4px solid rgba(128, 128, 128, 0.836);
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
}
.menu 
{
    width:100%;
    box-sizing: border-box;
    background-color: #0d1825f3;
  
 
}
li img 
{
    width:80px;
    cursor:pointer;
}
ul li 
{
    display:inline-block;
    margin:5px;
    margin-right:105px;
    color:white;
    padding:30px 0;
    
}

.footer ul 
{
    text-align:center;
  margin:0;
  padding:0;
}
.footer ul li 
{
    padding:0;
    margin:5px 20px;
    cursor:pointer;
}
</style>
