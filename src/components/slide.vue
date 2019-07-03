<template>
    
   
<div class="main">

    <div class="content">
       <transition-group v-bind:name= "animName">

           
 <div v-for= "number in [currentNumber]" v-bind:key="number" class="slider">

<img id="slidesIMG" v-bind:src="image[currentNumber]">

  </div>

</transition-group>

<!-- TEXT SLIDER -->
<transition-group name="textSlide">
<div v-for= "number in [currentNumber]"  v-bind:key="number" class="textSlider">
<img id="slideText" v-bind:src="text[currentNumber]">
<h1>{{info1[currentNumber]}} <br> {{info2[currentNumber]}}</h1>
<button>{{buttonText[currentNumber]}}</button>
</div>
</transition-group>



<img  v-on:click= "nextImg"   id="arrowR" src="https://image.flaticon.com/icons/svg/271/271228.svg">
<img  v-on:click= "previous" id="arrowL" src="https://image.flaticon.com/icons/svg/271/271220.svg">
</div>
</div>


    
</template>

<script>
export default {
data:function ()
{
    return {
        info1:['PREPARE', 'placeHold','placeHold','placeHold','placeHold'],
        info2:["TO GO DARK", 'placeHold','placeHold','placeHold','placeHold'],
        buttonText:["WATCH TRAILER", 'placeHold','placeHold','placeHold','placeHold'],
        text:['https://bnetcmsus-a.akamaihd.net/cms/gallery/BVNCIG8Q1AG91559235500667.png',"https://bnetcmsus-a.akamaihd.net/cms/gallery/2y/2Y086ONS2W8I1548874449028.png",'https://bnetcmsus-a.akamaihd.net/cms/gallery/IM557Q10Z43T1541100890908.png',"https://bnetcmsus-a.akamaihd.net/cms/gallery/1JIM3UV73ZJ21562007919980.png","https://bnetcmsus-a.akamaihd.net/cms/gallery/7SXTFNIW5YP11561596097087.png"],
        currentNumber:0,
        timer:null,
        animName:"slideForwards",
        
        image:[ "https://bnetcmsus-a.akamaihd.net/cms/gallery/GXD4JNW026CS1559235465911.jpg" ,"https://bnetcmsus-a.akamaihd.net/cms/gallery/CKZ5QSH3FUKX1548873953399.jpg"  ,"https://bnetcmsus-a.akamaihd.net/cms/gallery/6BVTRM03YOXE1541100891084.jpg","https://bnetcmsus-a.akamaihd.net/cms/gallery/3AIPM0OPFGOY1562008099385.jpg", "https://bnetcmsus-a.akamaihd.net/cms/gallery/RNICIQUDGMF51561595505381.jpg"]}
},

mounted: function ()
{
    this.startRotation();
},

methods:{
startRotation: function ()
{
 this.timer= setInterval(this.next, 5000)
},
next: function ()
{ 

  this.animName="slideForwards"
   if (this.currentNumber==this.image.length-1)
   {
       this.currentNumber=0;
   }
   else
{this.currentNumber=this.currentNumber+1;}
},
nextImg: function ()
{ 
    
    this.animName="slideForwards"
   clearTimeout(this.timer);
 this.timer = null;
   if (this.currentNumber==this.image.length-1)
   {
       this.currentNumber=0;
   }
   else
{this.currentNumber=this.currentNumber+1;}
},


previous: function () 
{
    this.animName="slideBackwards"
      clearTimeout(this.timer);
 this.timer = null;
    if (this.currentNumber==0)
    {
        this.currentNumber=this.image.length-1
    }
    else 
    {
        this.currentNumber=this.currentNumber -1 ;
    }
    
},




}
}
</script>

<style scoped>

.textSlider
{
    
 
background-size:500px;
height:100%;
width:100%;
cursor: pointer;
    position:absolute;
   top:60px;
 padding:70px 120px;
 font-family: 'Montserrat', sans-serif;
 font-size:35px;
 color:white;
}

.textSlider h1 
{
    margin:0;
}

#slideText 
{
   
    width:260px;
   top:50px;
    left:122px;
    cursor: pointer;
}

#arrowL
{
    width:20px;
    float:left;
    cursor: pointer;
        background-color: rgba(28, 106, 207, 0.767);
    padding:10px;
    border:.1px solid silver;
    margin:200px 10px;
    opacity:.8;
    position:relative;
     margin-left:20px;
   margin-top:250px;
   margin-bottom:0;
   height:80px;
     transition:all .3s;
     z-index:1;
     display:none;
}

#arrowR 
{
      width:20px;
    float:right;
    cursor: pointer;
         background-color: rgba(28, 106, 207, 0.767);
    padding:10px;
    border:.1px solid silver;
    margin:200px 10px;
    opacity:.8;
    position:relative;
     margin-left:20px;
   margin-top:250px;
   margin-bottom:0;
   height:80px;
  transition:all .3s;
  z-index:1;
    display:none;
}

.main:hover  #arrowL
{
    display:block;
  
}

.main:hover  #arrowR
{
    display:block;
  
}


#arrowR:hover 
{
  opacity:1;
  background-color: rgb(26, 137, 241);
}

#arrowL:hover 
{
   opacity:1;
  background-color: rgb(26, 137, 241);
}

.textSlide-enter
{
    opacity:0;
}

.textSlide-enter-active
{
    animation:slide-in .5s;
    transition:opacity .5s;
    animation-delay: .5s;
    transition-delay: .5s;

}



.main 
{
 height:600px;

  overflow:hidden;
    margin:0;
    padding:0;
    position:relative;
   background:rgb(20, 29, 54);
   z-index:-9999;
  max-width:2500px;
  margin:auto;
}

.content 
{
  
    margin:auto;
  

}

@media (max-width:2500px)
{
    .content 
    {
        width:100%;
    }
}


.slider 
{



}

#slidesIMG 
{
    
    
    margin:0;
    padding:0;
    position:absolute;
    top:0px;
    z-index:-999;
    overflow: hidden;
   left:-500px;
   overflow:hidden;
    
}

button {
    display: inline-block;
    position: relative;
    background-color: #0e86ca;
    border: solid 1px #00aeff;
    font-family: "Open Sans",Helvetica,Arial,sans-serif;
    font-size: 18px;
    font-weight: 400;
    color: #fff;
    padding: 10px 50px;
    text-decoration: none;
    text-align: center;
    cursor: pointer;
    transition: color .2s,background-color .2s,border-color .2s;
}
button:hover 
{
    background-color:#066ba5
}

@media (min-width:1920px)
{
    #slidesIMG 
    {
        left:0;
    }
}
.slideForwards-enter 
{
 overflow: hidden;
 opacity:0;
}

.slideForwards-enter-active  {

 
animation:slide-in 1s;
transition:opacity 1s;

position:relative;



}

.slideForwards-leave-active
{
  
animation:slide-out 1s;
position:relative;


}
.slideForwards-leave
{


}

@keyframes slide-in 
{
    from{

        transform:translateX(500px);
   
    }
    to 
    {
        transform:translateX(0);
        
    }
}

@keyframes slide-out
{
    from{

        transform:translateX(0);

    }
    to 
    {
        transform:translateX(-500px);
     
    }
}

/* BACKWARDS SLIDE ANIM */

.slideBackwards-enter 
{
opacity: 0;

}

.slideBackwards-enter-active  {


 
animation:slide-out-in 1s;
transition: opacity 1s;

position:relative;



}

.slideBackwards-leave-active
{
  
animation:slide-out-out 1s;
position:relative;


}
.slideBackwards-leave
{


}

@keyframes slide-out-in 
{
    from{

        transform:translateX(-500px);
      
    }
    to 
    {
        transform:translateX(0);
        
    }
}

@keyframes slide-out-out
{
    from{

        transform:translateX(0);
  
    }
    to 
    {
        transform:translateX(500px);
       
    }
}



@media (max-height:920px)
{
    .main 
    {
   height:600px;
    }

}

@media (min-height:921px)
{
.main {
    height:66%;
    max-height:700px;
}
}

</style>
