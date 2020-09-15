<template>
  <div class="shoplist about">
      <form action="">
    <div class="row">
      <label>Name</label>
       <input type="text" placeholder="Enter Name" v-model="put.input1" />
      <label>Amount</label>
      <input type="text" placeholder="Enter amount"  v-model="put.input2" />
    </div>
    <div class="row buto">
      <button class="btn btn-primary" @click.prevent="addT" :disabled="!put.input1 && !put.input2 ">Add</button>
      <button class="btn1 btn-primary del">Delete</button>
      <button class="btn2 btn-primary clear">Clear</button>
    </div>
      </form>
   <div class="list  row" v-for="out in output" v-bind:key="out.done" >
      <!--<h3>   {{put.output}}</h3>
         <h4>: {{put.output2}}</h4> -->
       <h3>   {{out.words}}  : ({{out.wo}})
       </h3>
      
   </div>
  </div>
</template>
<script>
export default {
    name:"shoplist",
     data() {
    return {
        put:{
        input1:" ",
        input2:" ",
        
        
      // output2:" "
    },
    output:[
            {
            words:"meat",
            wo:3,
            done:false},
            {
            words:"cake",
            wo:2,
            done:false}
            ]
    }},
    
    methods:{
addT(){
 //var txt=this.put.input1;
   // var num=this.put.input2;
   // txt=txt.toLowerCase();
    //this.$router.push("/recipes");
   // this.put.output=txt;
    //this.put.output2=num;
    this.output.push({ words:this.put.input1, wo:this.put.input2,done: false });
      this.put.input1 = "";
      this.put.input2 = "";
}
    }
}
</script>
<style scoped>
.about {
  margin-top: 20px;
  float: left;
  margin-left: 40px;
}
.about .row label {
  font-weight: bold;
  margin: 25px;
  font-size: 24px;
}
.about .row input {
    margin-top:25px !important;
  margin: 8px;
  width: 220px;
  height: 30px;
}
.about .buto button {
  margin: 3px;
}
.about .buto .btn {
  background-color: darkcyan;
  border-radius: 5px;
  height: 35px;
  font-weight: bold;
  color: cornsilk;
  width: 60px;
}
.about .buto .btn1 {
  background-color: rgb(139, 0, 0);
  border-radius: 5px;
  height: 35px;
  font-weight: bold;
  color: cornsilk;
  width: 60px;
}
.about .buto .btn2 {
  background-color: blue;
  border-radius: 5px;
  height: 35px;
  font-weight: bold;
  color: cornsilk;
  width: 60px;
}
.list{
    border: 1px solid #DDD;
    margin-top: 2px ;
}
</style>
