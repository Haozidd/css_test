<template>
  <div id="container">
    <Bubble/>

  </div>
</template>

<script>
import Bubble from "@/components/Bubble";

export default {
  name: 'App',
  components: {
    Bubble
  }
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
}
body{
  width: 100%;
  height: 100vh;
  background:
      linear-gradient(150deg,rgba(0,0,0,.1),rgba(0,0,0,.1)),
      linear-gradient(150deg,plum,lemonchiffon);

  display: flex;
  justify-content: center;
  align-items: center;
}

#container {
  width: 200px;
  height: 400px;
  position: relative;

}
</style>
