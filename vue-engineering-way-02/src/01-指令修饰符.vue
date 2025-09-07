<script setup>
 const onKeydown = () => {
  console.log("onKeydown")
 }

 const onDivClick = () => {
  console.log("onDivClick")
 }

 const onPClick = () =>{
  console.log("onPClick")
 }

</script>


<template>

  <input type="text" @keydown.enter="onKeydown"/>
  
  <div @click="onDivClick">

    <a href="https://www.baidu.com/" @click.prevent.stop>百度一下</a>

    <p @click.stop="onPClick"></p>

  </div>
</template>

<style scoped>
div {
  width: 400px;
  height: 200px;
  background: plum;
}
div a {
  display: block;
  width: 100px;
  text-decoration: none;
  background: tomato;
  text-align: center;
  color: #fff;
}
div p {
  width: 200px;
  height: 100px;
  background: rebeccapurple;
}
</style>
