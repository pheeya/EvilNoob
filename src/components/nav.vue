<template>
    <div class="main">
     

      <div class="blackNav">Evil Noobs</div> 

  <ul id="mainNav">
  
            
   
      <li id="imgSRC"><img src="https://media.discordapp.net/attachments/584665267078955009/596189236286193665/mascot.png"></li>
      <li></li>
      <li></li> 
      <li v-on:click= "gamesMenu">GAMES▼</li>
      <li>SHOP</li>
      <li>NEWS</li>
      <li v-on:click= "esportsMenu">ESPORTS▼</li>
    <li id="rightTab" >My Account</li>
      <li id="rightTab">Support</li>
  </ul>

  <cmp-drop v-bind:showMenu= "menu"></cmp-drop>
  <cmp-drop2 v-bind:showMenu2="menu2"></cmp-drop2>
<cmp-List></cmp-List>

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


#imgSRC 
{
 
   margin:0;
  padding:0;
  

}
#imgSRC img 
{
  width:65px;
top:3px;
left:px;
  margin:0;
  padding:0;
  position: absolute;
}

.main 

{
  position: absolute;
  width:100%;
z-index:99;
  margin:0 auto;
border-bottom:1px solid rgba(255, 255, 255, 0.219);

}
.blackNav 
{
    width:100%;
    position:absolute;
 height:40.4px;
    background-color:black;
    display:none;
    color:white;
    text-align:center;
    font-size:25px;
    padding-top:10px;
    z-index:99;
    font-family: 'Open Sans', sans-serif;
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
      

max-width:1520px;
margin:auto;

  padding-bottom:13px;
}


.main #mainNav li
{
    padding:3px 0px;
    margin:0px 13px;
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
.blackNav 
{
  display:block;
}
}
</style>
