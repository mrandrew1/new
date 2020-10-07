<template>
  <div class="nav">
    <!-- <div class="leftmenu"> -->
    <li>
      <img src="https://vuejs.org/images/usave.png" alt="Logo" width="90px" />
    </li>
    <li><router-link to="/">Home </router-link></li>
    <li><router-link to="/about"> About&nbspus </router-link></li>
    <li><router-link to="/projects"> projects </router-link></li>
    <li class="prelast"></li>
    <li><router-link to="/contacts"> contacts </router-link></li>
    <!-- </div> -->
  </div>
</template>

<script>
export default {
  name: "Navbar",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  padding: 0;
  margin: 0;
}
.nav {
  /*генерирует flex-контейнер уровня блока*/
  display: -webkit-flex;
  display: flex;
  background-color: cadetblue;
  color: rgba(133, 216, 78, 0.918);
  flex-wrap: wrap;
  justify-content: space-evenly;
  width: 96%;
  margin: auto;
  border-radius: 45px;
  font-weight: 400;
  font-size: 1em;
}
.nav .prelast {
  flex-grow: 1;
  min-width: 0px;
}
.leftmenu {
  line-height: 1.3em;
  display: flex;
}
.rightmenu {
  line-height: 20pt;
  display: flex;
}
.nav li {
  margin: 1.2em;
  list-style-type: none;
}

.nav li :hover {
  border-bottom: 2px solid white;
}

@media screen and (max-width: 620px) {
  .nav {
    justify-content: center;
  }
  .prelast {
    display: none;
  }
  .nav li {
    width: 100%;
    margin: 0.3em;
  }
}
</style>
