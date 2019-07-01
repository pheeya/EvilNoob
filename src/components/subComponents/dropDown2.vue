<template>
    <transition name="fade"> <div v-if="showMenu2" class="main">
<div class="menu">
<ul>
    <h3 style="margin:0;padding:10px; color:white; font-weight:200;">EvilNoobs</h3>
    <li><img src="https://blznav.akamaized.net/img/esports/esports-overwatch-world-cup-43d00c39399a70b8.png"><h4>GAME1</h4></li>
    <li><img src="https://blznav.akamaized.net/img/esports/esports-hsm-5b1ed3fe5cf5d4f8.png"><h4>GAME2</h4></li>
    <li><img src="https://blznav.akamaized.net/img/esports/esports-sc2-32be849895ec4e7d.png"><h4>GAME3</h4>  </li>
    <li><img src="https://blznav.akamaized.net/img/esports/esports-overwatch-36d8f7f486d363c1.png"><h4>GAME5</h4>  </li>
    <li><img src="https://blznav.akamaized.net/img/esports/esports-wowwc-79e9589cf9355f17.png"><h4>GAME6</h4></li>
 

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
   
        
         props:['showMenu2']
     
   

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

hr 
{
    border:.5px solid rgba(128, 128, 128, 0.836);
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
    width:150px;
    cursor:pointer;
}
ul li 
{
    display:inline-block;
    margin:5px;
    margin-right:10px;
    color:white;
    padding:30px 0;
    margin-bottom:0;
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

@media (max-width:870px)
{
    .main
    {
        display:none;
    }
}
</style>
