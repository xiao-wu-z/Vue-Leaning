<script setup>
  import { ref } from 'vue'
  const msg = ref("Hello World!")
  const src = ref('<span style="color:red;">Hello Vue3+Vite</span>')
  const url = ref('https://www.baidu.com/')
  const count = ref(0)
  const addOne = () => {
    count.value++
  }
  const addThree = (num) => {
    count.value+=num
  }
</script>

<template>
  <h1>{{ msg }}</h1>
  <div v-html="src"></div>
  <a v-bind:href="url">百度一下</a>
  <div>{{ count }}</div>
  <button v-on:click="count++">+1</button>
  <button @click="addOne">+1</button>
  <button @click="addThree(3)">+3</button>
</template>

<style scoped>

</style>
