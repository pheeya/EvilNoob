<template>
    
    <div class="worlds">
 <transition name="fade"> <div v-on:click="next" v-for= "number in [counter]" :key= "number" v-bind:style="{ backgroundImage: 'url(' + image[counter] + ')' }" class="main">

</div></transition>



<div class="content">
<h1>Create worlds</h1>
<p>Learn more about Careers at Blizzard</p>


<button>Explore Careers</button>
</div>
    </div>
</template>

<script>
export default {
data: function ()
{
    return {
       
        counter:0,
        image:["https://bnetcmsus-a.akamaihd.net/cms/page_media/CX2HSQAV75TE1541463093237.jpg","https://bnetcmsus-a.akamaihd.net/cms/page_media/6Q88KQY7PY161541463093255.jpg"]
    }
},
mounted: function ()
{
    this.startRotation();
},
methods: 
{
    startRotation:function ()
    {
   this.timer= setInterval(this.next, 5000)
    },
    next: function ()
    {
        if (this.counter<this.image.length-1){
        this.counter=this.counter+1;}
        else {this.counter=0};
 
    }
}
}
</script>

<style scoped>

.fade-enter 
{
    opacity:0;
}
.fade-enter-active
{
    transition:opacity 1s;
    
}

.fade-leave 
{
    
}

.fade-leave-active
{
    transition:opacity 1s;
    opacity:0;
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
.worlds p 
{
    color:rgb(221, 216, 216);
    font-size:23px;
  
}
.worlds h1
{
    font-weight: 300;
    font-size:40px;
    margin:0;
}
.worlds 
{
    font-family: 'Montserrat', sans-serif;
    color:white;
   -moz-box-sizing: border-box; 
    -webkit-box-sizing: border-box; 
     box-sizing: border-box; 
  position:relative;
  max-width:1600px;

  margin:auto;
     border-bottom:2px solid rgb(8, 156, 255);
}
.main 
{
    font-family: 'Montserrat', sans-serif;
    color:white;
   -moz-box-sizing: border-box; 
    -webkit-box-sizing: border-box; 
     box-sizing: border-box; 
 


    background-position: right;

    background-size:cover;
    position: absolute;
    z-index:-99;
    
   height:431px;
       
      text-align:center;
 


 width:100%;
     
    background-repeat: no-repeat;
     margin:auto;
margin-right:0;
}

.content 
{
   width:100%;
   margin:auto;
    padding:130px 50px;
 
  margin-right:0;
   -moz-box-sizing: border-box; 
    -webkit-box-sizing: border-box; 
     box-sizing: border-box; 
     margin-bottom:30px;
     padding-bottom:0;
}


</style>
