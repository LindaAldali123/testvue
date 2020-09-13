<template>
<div class="log-in">
      <div class="container">
    <div class="row">
<label>E-Mail: </label>
<input type="text"/>
</div>
<div class="row">
<label>Password:</label>
<input type="text"/>
</div>
<div class="row">
    <button class="btn btn-primary">Sign Up</button> |
    <button class="btn btn-primary">switch to Login</button>
</div>
    </div>
</div>
</template>
<script>
export default{
name:"log"
}
</script>
<style >
.log-in{
    float: left;
    margin:180px;
    margin-left: 180px !important;
}
.log-in .row{
    margin-top: 20px;
}
.log-in label{
font-weight: bold;
font-size: 25px;
}
.log-in input{
    width:290px;
    height: 30px;
}
.log-in .row button{
    color:honeydew;
    font-weight: bold;
    height: 40px;
    margin:20px;
    background-color: rgb(80, 148, 204);
    border-radius: 5px;
     font-size: 18px;
}
</style>