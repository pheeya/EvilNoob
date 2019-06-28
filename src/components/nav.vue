<template>
    <div class="main">
     

        
  
  <ul id="mainNav">
      <li>LOGO</li>
      <li>GAMES</li>
      <li>SHOP</li>
      <li>NEWS</li>
      <li>ESPORTS</li>
    <li id="rightTab">My Account</li>
      <li id="rightTab">Support</li>
  </ul>





</div>
    
</template>

<script>
export default {
data:function ()
{
    return {
        
        currentNumber:0,
        timer:null,
        
        image:["http://pavbca.com/walldb/original/4/d/2/10125.jpg", "http://pavbca.com/walldb/original/d/b/a/10118.jpg", "http://pavbca.com/walldb/original/8/4/6/10119.jpg"]}
}





}
</script>

<style scoped>








.main #mainNav
{
    padding:2px 35px;
    margin:0;
    list-style-type: none;
   border-bottom:.1px solid silver;
 background-color:rgba(49, 49, 49, 0.836);
     color: rgba(255, 255, 255, 0.7);
     
 
z-index:9999;
position:relative;
   
  
}

.main #mainNav li
{
    padding:0;
    margin:15px 19px;
    list-style-type: none;
  font-family: 'Open Sans', sans-serif;
   
    font-size:20px;
    font-weight: 500;
    display:inline-block;
cursor:pointer;

}
#rightTab
 {
     float:right;
 }

</style>
