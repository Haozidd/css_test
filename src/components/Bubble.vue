<template>
  <div id="bubble-container">
    <div id="bubble"></div>
    <div id="bubble-shadow"></div>
  </div>
</template>

<script>
export default {
  name: "Bubble"
}
</script>

<style scoped lang="scss">
#bubble-container{
  display: flex;
  flex-flow: column nowrap;
  align-items: center;

  width: 100%;
  height: 70%;
}
#bubble{
  width: 200px;
  height: 200px;

  background: radial-gradient(
          circle at 75% 30%,
          white 6px,
          rgb(239, 135, 182) 7%,
          skyblue 60%,
          plum 100%
  );
  border-radius: 50%;
  box-shadow: inset 0 0 20px #fff,
  inset 10px 0 46px #eaf5fc,
  inset 80px 10px 60px #eacde6,
  inset -20px -60px 46px #f9f6de,
  inset 0px 50px 140px #f9f6de,
  0px 0px 30px white;

  animation: bubble 4s ease-in-out infinite;
}
#bubble-shadow{
  background: gray;
  opacity:.6;
  margin-top: 20px;
  width: 150px;
  height: 40px;
  border-radius: 50%;

  animation: bubble-shadow 4s ease-in-out infinite;

}
@keyframes bubble-shadow {
  0%,100%{
    transform: scale(.8);
  }
  50%{
    transform: scale(1.4);
    opacity: .3;
  }
}

@keyframes bubble{
  0%,100%{
    transform: translateY(0);
  }
  50%{
    transform: translateY(-80px);
    box-shadow: inset 0 0 20px #fff,
    inset -10px 0 46px #eaf5fc,
    inset -40px -10px 60px #eacde6,
    inset -0px 60px 46px #f9f6de,
    inset 0px -50px 140px #f9f6de,
    0px 0px 90px white;
  }
}


</style>