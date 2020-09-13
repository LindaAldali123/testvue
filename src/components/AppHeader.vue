<template>
  <div class="row header">
    <ul>
      <router-link to="/" tag="li" exact>
        <a>Shoping List</a>
      </router-link>
      <router-link to="/about" tag="li">
        <a>Recipes</a>
      </router-link>
      <router-link class="left" to="/login" tag="li" replace>
        <a>Logout</a>
      </router-link>
   <!-- <div>
  <b-dropdown id="dropdown-offset" offset="25" text="Offset Dropdown" class="m-2">
    <b-dropdown-item href="#">Action</b-dropdown-item>
    <b-dropdown-item href="#">Another action</b-dropdown-item>
    <b-dropdown-item href="#">Something else here</b-dropdown-item>
  </b-dropdown>
</div> -->

    </ul>
  </div>
</template>
<script>
export default {
  name: "AppHeader"
};
</script>
<style lang="scss" scoped>
.header {
  background-color: rgb(230, 224, 224);
  overflow: hidden;
  border-radius: 5px;
  ul {
    float: left;
    width: calc(100%-200px);
    margin: 0;
    li {
      padding: 20px;
      display: inline-block;
      font-size: 18px;
      a {
        text-decoration: none;
      }
    }
  }
  .header ul .left {
    margin-left: 120px !important;
  }
}
</style>