<template>
    <div class="main">
   
 <div  class="parrallax">
       <transition-group v-bind:name= "animName">   
 <div v-for= "number in [currentNumber]" v-bind:key="number" class="slider">

<img id="slidesIMG" v-bind:src="image[currentNumber]">

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
        
        currentNumber:0,
        timer:null,
        animName:"slideForwards",
        
        image:["https://bnetcmsus-a.akamaihd.net/cms/gallery/KO27VQL5M8EL1560816589144.jpg", "https://bnetcmsus-a.akamaihd.net/cms/gallery/RNICIQUDGMF51561595505381.jpg", "https://bnetcmsus-a.akamaihd.net/cms/gallery/RNICIQUDGMF51561595505381.jpg"]}
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

.slider 
{
width:100%;
width:100%;
background:red;

}

#slidesIMG 
{
    
    
    margin:0;
    padding:0;
    position:absolute;
    top:0px;
    z-index:-999;
    overflow: hidden;
   overflow:-moz-hidden-unscrollable;
 
 
}
.slideForwards-enter 
{
 overflow: hidden;
}

.slideForwards-enter-active  {

 
animation:slide-in 1s;
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

        transform:translateX(100%);
   
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
        transform:translateX(-100%);
     
    }
}

/* BACKWARDS SLIDE ANIM */

.slideBackwards-enter 
{


}

.slideBackwards-enter-active  {

 
animation:slide-out-in 1s;
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

        transform:translateX(-180%);
      
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
        transform:translateX(100%);
       
    }
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
     z-index:0;
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
  z-index:0;
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
.parrallax
{
  
    
 top:-60px;
position:relative;

    height:600px;
    overflow:hidden;
}
.main 
{
 height:540px;
    
  
    margin:0;
    padding:0;
    position:relative;
}

</style>
