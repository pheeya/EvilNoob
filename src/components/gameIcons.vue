<template>
    <div class="main">
        <div class="content">
            <img v-on:click= "moveLeft" id="arrowR" src="https://image.flaticon.com/icons/svg/271/271228.svg">
<img v-if= "movement!=0" v-on:click= "moveRight" id="arrowL" src="https://image.flaticon.com/icons/svg/271/271220.svg">
<img  v-if="movement==0" id="replacer">
<h1>Games </h1> <p>  view all games ></p> <h2>Blizzard</h2>

<div class="gameIcons">

    <ul>
       <li v-for= "(img,index) in source" key:index v-bind:style= "{left:movement +'px'}"><img :src=img> </li>
  
      </ul>
</div>
</div>
<div class="footer">
<h2>All games, one app:Blizzard Battle.net Desktop AppStay connected:Blizzard Battle.net Mobile App</h2>
</div>
  
    </div>
</template>

<script>
export default {
data: function ()
{
    return {movement:"0",
    source:["https://bnetcmsus-a.akamaihd.net/cms/page_media/M7G2U62LWFRW1506441174974.jpg", "https://bnetcmsus-a.akamaihd.net/cms/page_media/XMG50RXK21EC1506441173958.jpg","https://bnetcmsus-a.akamaihd.net/cms/page_media/A7ZYBYYMLVK81506441173875.jpg", "https://bnetcmsus-a.akamaihd.net/cms/page_media/ZHCSQYYYZFSQ1541021628936.jpg"
    ,"https://bnetcmsus-a.akamaihd.net/cms/page_media/IRV46MHUTP0B1541021628836.jpg",
    "https://bnetcmsus-a.akamaihd.net/cms/page_media/F2B8X5LJKA3G1506441173755.jpg",
    "https://bnetcmsus-a.akamaihd.net/cms/page_media/X3MOVXG6FYN31506441174058.jpg",
    "https://bnetcmsus-a.akamaihd.net/cms/page_media/F2B8X5LJKA3G1506441173755.jpg",
    "https://bnetcmsus-a.akamaihd.net/cms/page_media/X3MOVXG6FYN31506441174058.jpg"]}
},
methods: {

  moveLeft: function ()
  {
      this.movement=this.movement - 184;
  },
  moveRight: function ()
  {
  this.movement=this.movement +184;
  },
}
}
</script>

<style scoped>


.footer 
{
  
    position:absolute;
    width:100%;
    text-align:center;
    bottom:0;
    border-top:1px solid rgba(45, 117, 226, 0.726);
   border-bottom:1px solid rgba(45, 117, 226, 0.726);
    font-size:12.5px;
    font-weight:normal;
    
    
}
.footer h2 
{
 
    font-weight:300;
        color: rgba(255, 255, 255, 0.8);
}


h1,p  
{
display:inline-block;
margin-bottom:15px;
margin-right:3px;
margin-top:0;
font-weight:300;
}
p 
{
     color: #00aeff;
    cursor:pointer;
}
h2 
{
    margin:20px 0 20px 38px;
    padding:0;
    color:gray;
    font-weight: 300;
    font-size:18px;
    
}

.main 
{
   font-family: 'Montserrat', sans-serif;
   font-weight:300;
    margin:0;
    padding:0;
     color:white;
     position:relative;
     top:0;
background-image:url("https://d9me64que7cqs.cloudfront.net/images/common/background-generic-landscape-short-c67b55f50ca032607997398840751185782dd86436566617ed80dd553f62a890f554ca38ef1de26c6d60b4976ebea6145b9916091073d06823aa9853a093f3e7.jpg");
background-size:cover;
background-position:center;

border-top:0.3px solid rgb(9, 155, 240);
padding:80px 0;
font-weight: bold;

}
.gameIcons ul 
{
    list-style-type: none;
    display:flex; 
    margin:0;
    padding:0;
 margin-left:40px;
 position: relative;
 overflow: hidden;
 margin-bottom:50px;
}
.content 
{
    
    font-weight: 400;
}
.gameIcons ul li 
{
    
margin-right:15px;
       height:200px;
    width:167px;
    border:1px solid silver;
    position:relative;
    transition: all .2s ease-in-out;
   
  display:inline-block;
}

.gameIcons img 
{
height:200px;
width:167px;
}


#arrowL
{
   
    float:left;
    cursor: pointer;
    background-color:rgba(16, 95, 212, 0.5);
    padding:10px;
    border:.1px solid silver;
    opacity:.8;
    position:relative;  
    top:190px;
    width:15px;
    height:50px;
    
}

#arrowR 
{
    float:right;
    cursor: pointer;
    background-color:rgba(16, 95, 212, 0.5);
    padding:10px;
    border:.1px solid silver;
    opacity:.8;
    position:relative;  
    margin-top:190px;
    width:15px;
    height:50px;




    
}

#replacer 
{
  float:left;
    
    background-color:gray;
    padding:10px;
    border:.1px solid silver;
    opacity:0;
    position:relative;  
    top:100px;
    width:15px;
    height:50px;

}
</style>
