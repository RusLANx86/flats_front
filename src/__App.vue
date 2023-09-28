<template>
  <div id="header" class="block">
    <h1>
      Шапка
    </h1>
  </div>
  <div id="menu" class="block">
    Навигация
  </div>
  <div id="content" class="block">
    <div id="left_panel" class="block">
      Левая панель
    </div>
    <div id="right_panel" class="block">
      Правая панель
    </div>
  </div>
  <div id="foot" class="block">
    Подвал
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {}
}
</script>

<style>
body {
  //box-sizing: border-box;
  background: darkcyan;
}
.block{
  margin: 5px;
  background: cadetblue;
  border: solid 2px blue;
}
#content {
  height: 650px;
}
#header {
  min-height: 100px;
}
#menu {
  min-height: 50px;
}
#left_panel {
  float: left;
  height: 600px;
  width: 15%;
}
#right_panel {
  height: 600px;
}
#foot {
  min-height: 90px;
}

</style>
