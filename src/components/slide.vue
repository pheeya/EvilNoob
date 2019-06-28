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
        
        image:["http://pavbca.com/walldb/original/4/d/2/10125.jpg", "http://pavbca.com/walldb/original/d/b/a/10118.jpg", "http://pavbca.com/walldb/original/8/4/6/10119.jpg"]}
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
    width:100%;
    max-height: 600px;
    margin:0;
    padding:0;
    position:absolute;
    top:0px;
    z-index:-999;
    overflow: hidden;
 
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

        transform:translateX(-100%);
      
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
        background-color: rgba(0, 0, 0, 0.4);
    padding:10px;
    border:.1px solid silver;
    margin:200px 10px;
    opacity:.8;
    position:relative;
     margin-left:20px;
   margin-top:15%;
   margin-bottom:0;
   height:80px;
     transition:all .3s;
}

#arrowR 
{
      width:20px;
    float:right;
    cursor: pointer;
        background-color: rgba(0, 0, 0, 0.4);
    padding:10px;
    border:.1px solid silver;
    margin:200px 10px;
    opacity:.8;
    position:relative;
     margin-left:20px;
   margin-top:15%;
   margin-bottom:0;
   height:80px;
  transition:all .3s;
}


#arrowR:hover 
{
         background-color: rgba(53, 53, 53, 0.4);
}

#arrowL:hover 
{
      background-color: rgba(53, 53, 53, 0.4);
}
.parrallax
{
  
    
 top:-60px;
position:relative;

    height:37.5vw;
}
.main 
{

    height:37.5vw;
  
    margin:0;
    padding:0;
    position:relative;
}

</style>
