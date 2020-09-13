<template>
  <div class="about">
    <div class="row">
    <label>Name</label>
    <label>Amount</label>
    
    </div>
    <div class="row">
    <input type="text">
    <input type="text">
    </div>
    <div class="row buto">
       <button class="btn btn-primary">Add</button>
        <button class="btn1 btn-primary">Delete</button>
         <button class="btn2 btn-primary">Clear</button>
    </div>
   
    
  </div>
</template>
<script>

export default {
  
}
</script>
<style scoped>
.about{
  margin-top: 20px;
  float: left;
  margin-left: 40px;
}
.about .row label{
  font-weight: bold;
  margin:25px;
  font-size:24px;
}
.about .row input{
  margin:8px;
  width:220px;
  height: 30px;
}
.about .buto button{
  margin:3px;
}
.about .buto .btn{
background-color: darkcyan;
border-radius: 5px;
height: 35px;
font-weight: bold;
color: cornsilk;
width:60px;
}
.about .buto .btn1{
  background-color: rgb(139, 0, 0);
  border-radius: 5px;
height: 35px;
font-weight: bold;
color: cornsilk;
width:60px;
}
.about .buto .btn2{
  background-color: blue;
  border-radius: 5px;
height: 35px;
font-weight: bold;
color: cornsilk;
width:60px;
}
</style>
