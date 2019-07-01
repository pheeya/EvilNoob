<template>
    <div class="main">
     

        
  
  <ul id="mainNav">
      <li>LOGO</li>
      <li v-on:click= "menu=!menu">GAMES▼</li>
 
      <li>SHOP</li>
      <li>NEWS</li>
      <li>ESPORTS▼</li>
    <li id="rightTab" style="font-size:17px;">My Account</li>
      <li id="rightTab" style="font-size:17px;">Support</li>
  </ul>

  <cmp-drop v-bind:showMenu= "menu"></cmp-drop>



</div>
    
</template>

<script>
import drop from "./subComponents/dropDown"
export default {
components: 
{
  cmpDrop:drop
},

data:function ()
{
    return {
        menu:true,
        currentNumber:0,
        timer:null,
        
        image:["http://pavbca.com/walldb/original/4/d/2/10125.jpg", "http://pavbca.com/walldb/original/d/b/a/10118.jpg", "http://pavbca.com/walldb/original/8/4/6/10119.jpg"]}
}





}
</script>

<style scoped>








.main #mainNav
{
    padding:2px 42px;
    margin:0;
    list-style-type: none;

color:rgba(231, 231, 231, 0.815);
     
     background: transparent;
    white-space: nowrap;
z-index:999;
position:relative;
      border-bottom:1px solid rgba(255, 255, 255, 0.219);
  
}


.main #mainNav li
{
    padding:0;
    margin:15px 15px;
    list-style-type: none;
  font-family: 'Open Sans', sans-serif;
   
    font-size:20px;
    font-weight: 500;
    display:inline-block;
cursor:pointer;
transition:all .2s;
}

.main #mainNav li:hover 
{
  color:white;
}


#rightTab
 {
     float:right;
     
 }

</style>
