<template>
    <div class="main">
        <div class="content">



<h1>Top Stories</h1>
<p>view all stories</p>
<div class="tiles">
<ul>
    <!-- 1st card -->
<div class="card">
    <img v-bind:src= "imgLink1">
    <p>INSIDE BLIZZARD</p>
    <h3>CALL OF DUTY®: MODERN WARFARE® LAUNCHING OCTOBER 25 ON BLIZZARD BATTLE.NET</h3>
    </div>
 <!-- 2nd card -->
 <div class="card">
    <img v-bind:src= "imgLink1">
    <p>INSIDE BLIZZARD</p>
    <h3>CALL OF DUTY®: MODERN WARFARE® LAUNCHING OCTOBER 25 ON BLIZZARD BATTLE.NET</h3>
    </div>
<!-- last card -->
     <div class="card">
    <img v-bind:src= "imgLink1">
    <p>INSIDE BLIZZARD</p>
    <h3>CALL OF DUTY®: MODERN WARFARE® LAUNCHING OCTOBER 25 ON BLIZZARD BATTLE.NET</h3>
    </div>
</ul>
</div>
</div>
    </div>



</template>


<script>
export default {
 
    props:["imgLink1", "imgLink2", "imgLink3"]
}
</script>

<style scoped>
.main 
{
    font-family: 'Montserrat', sans-serif;
    background-image:url("https://d9me64que7cqs.cloudfront.net/images/root/top-stories-events_section-background_lrg-b81ac9b879c693e7e05f049b5f913706fe0bae6e45523140fcf45aa3fac871c488749bf6fe38e89c9f84d372f690e485652fed36d04d5dbb083d99ea38813b4b.jpg");
background-size:cover;
background-position:center;
height:600px;
   margin:0;
   padding:80px 0;
    box-sizing: border-box;
            -webkit-box-sizing: border-box;
            -moz-box-sizing: border-box;
            color:white;
              border-bottom:1px solid rgba(45, 117, 226, 0.726);
}
.main h1
{
 
     font-weight:400;
   font-size:100;
    margin:0;
    
    
}
.content 
{
    padding:10px 50px;
    overflow:hidden;
 
    width:1300px;
    margin:auto;
}

.card 
{
       margin-top:20px;
        position: relative;
    background-color: #0d63c573;
    color: #fff;
    overflow: hidden;
    cursor: pointer;
    transition: color .2s,background-color .2s,border-color .2s;


    max-width:427.1px;
    min-width:200px;
    border:1px solid rgba(45, 117, 226, 0.726);
  max-height:399px;
  margin:10px;
  overflow:hidden;
  transition:all .3s;
}
.card img 
{
    width:100%;
    background-size: cover;
    background-position: center;
    overflow: hidden;
    transition: all .3s;
   
}
.card p 
{
    margin-left:10px;
   color: rgba(255, 255, 255, 0.5);
}
.card h3 
{
    margin-left:10px;
     padding-bottom:40px;
}
.card:hover img 
{
    transform:translateX(-4%);
width:110%;

}
.card:hover 
{
    height:100%;
    background-color: #1768c4a4;
     border:1px solid rgba(46, 130, 255, 0.712);
}
.tiles ul 
{
    margin:0;
    padding:0;
    display:flex;
    transition:all .3s;
    
    
}
h1,p 
{
    display:inline-block;
    margin:20px;
}
p 
{
        color: #00aeff;
        cursor: pointer;
}

@media (max-width:1400px)
{
    .content 
    {
        width:unset;
        overflow: hidden;
        padding-left:5px;
    }
}
</style>
