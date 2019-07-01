<template>
    <div class="main">
     

        
 <div><img id="smolMenu" v-on:click= "showList=!showList" 
 src="https://c.s-microsoft.com/en-us/CMSImages/icon_menu_new.png?version=2e17c0b9-dc99-1d59-c64d-0be30696e854"> 
 <hr id="smolHR" style="margin-top:50px;position:absolute;z-index:99; width:99%">
 </div>
  <ul id="mainNav">
  
   
   
      <li>LOGO</li>
      
      <li v-on:click= "gamesMenu">GAMES▼</li>
      <li>SHOP</li>
      <li>NEWS</li>
      <li v-on:click= "esportsMenu">ESPORTS▼</li>
    <li id="rightTab" >My Account</li>
      <li id="rightTab">Support</li>
  </ul>

  <cmp-drop v-bind:showMenu= "menu"></cmp-drop>
  <cmp-drop2 v-bind:showMenu2="menu2"></cmp-drop2>
<cmp-List :listMenu="showList"></cmp-List>

</div>
    
</template>

<script>
import drop from "./subComponents/dropDown1"
import drop2 from "./subComponents/dropDown2"
import list from "./subComponents/listMenu"
export default {
components: 
{
  cmpDrop:drop,
  cmpDrop2:drop2,
  cmpList:list
},

data:function ()
{
    return {
      showList:false,
       listMenu:false,
      menu2:false,
        menu:false,
        currentNumber:0,
        timer:null,
        
        image:["http://pavbca.com/walldb/original/4/d/2/10125.jpg", "http://pavbca.com/walldb/original/d/b/a/10118.jpg", "http://pavbca.com/walldb/original/8/4/6/10119.jpg"]}
},
methods: 
{
  gamesMenu:function ()
  {
    this.menu=!this.menu;
    this.menu2=false;
  },
  esportsMenu:function ()
  {
    this.menu2=!this.menu2;
   this.menu=false;
  }
}





}
</script>

<style scoped>



#smolHR 
{
  display:none;
}
#smolMenu 
{
  position:absolute;
  top:15px;
  
  margin:0;
  padding:0;
z-index:101;
width:50px;
 display:none;
 
cursor:pointer;
}




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
   display:inline-block;
    
    font-weight: 500;
   
cursor:pointer;
transition:all .2s;
font-size:20px;
margin-top:10px;
}

.main #mainNav li:hover 
{
  color:white;
}


#rightTab
 {
     float:right;
     font-size:15px;
     display:inline-block;
 }




@media (max-width: 870px) {

.main #mainNav 
{
display:none;
}
#smolMenu,#smolHR
{
  display:block;
}
}
</style>
