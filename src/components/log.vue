<template>
  <div class="log-in">
    <div class="container">
      <form @submit.prevent="userRegistration">
        <div class="form-group row">
          <label>E-Mail:</label>
          <input type="email" class="form-control" id="inputemail" v-model="user.email" />
        </div>
        <div class="form-group row">
          <label>Password:</label>
          <input type="password" class="form-control" id="inputpassword" v-model="user.password" />
        </div>
        <div class="row">
          <button type="submit" class="btn btn-primary" :disabled="!user.email ||  !user.password ">Sign Up</button> |
          <button class="btn btn-primary">switch to Login</button>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  name: "log",
  data() {
    return {
      user: {
        email: "",
        password: ""
      }
    };
  },
  methods: {
    userRegistration() {
      this.$router.push("/recipes");
    }
  }
};
</script>
<style >
.log-in {
  float: left;
  margin: 180px;
  margin-left: 180px !important;
}
.log-in .form-group {
  margin-top: 20px;
}
.log-in label {
  font-weight: bold;
  font-size: 25px;
}
.log-in input {
  width: 290px;
  height: 30px;
}
.log-in .row button {
  color: honeydew;
  font-weight: bold;
  height: 40px;
  margin: 20px;
  background-color: rgb(80, 148, 204);
  border-radius: 5px;
  font-size: 18px;
}
</style>