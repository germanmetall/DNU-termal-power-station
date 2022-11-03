<template>
  <div class="page">
    <div class="text text--medium text--center animate-text">
      Hey buddy, i think you got the wrong door.
      <br/>
      The leather-club is two blocks down.
    </div>
  </div>
</template>

<script setup>

</script>

<style lang="scss">
body{
  margin: 0;
  padding: 0;
}
.page{
  width: 100vw;
  overflow-x: hidden;
  min-height: 100vh;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  font-family: 'Courier New', Courier, monospace;
  font-size: 2rem;
  color: #212121;
  background-color: #dedede;
}
.text{
  &--big{
    font-size: 5rem;
  }
  &--medium{
    font-size: 3rem;
  }
  &--small{
    font-size: 1.75rem;
  }
  &--center{
    text-align: center;
  }
}
.animate-text{
  transition: .5s;
  transform: translate(0,0);
  color: #000;
  animation-name: text-moving;
  animation-duration: 10s;
  animation-timing-function: ease-in-out;
  animation-iteration-count: infinite;
  animation-fill-mode: forwards;
}
@keyframes text-moving{
  0%{
    transform: translate(0,0);
    color: #000;
  }
  10%{
    transform: translate(20%,-15vh);
    color: lightcoral;
  }
  33%{
    transform: translate(20%,-15vh);
    color: lightcyan;
  }
  43%{
    transform: translate(-5%,30vh);
    color: lightblue;
  }
  67%{
    transform: translate(-5%,30vh);
    color: lightgreen;
  }
  77%{
    transform: translate(0,0);
    color: lightpink;
  }
  100%{
    transform: translate(0,0);
    color: #000;
  }
}
</style>