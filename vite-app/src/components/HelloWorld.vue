<template>
  <div id="hello">我是hello 组件</div>
  <div>{{count}}</div>
  <button @click="count++">改变count</button>
</template>

<script setup lang="ts">
import { onBeforeMount, onBeforeUpdate, onMounted, onUpdated, ref } from 'vue';

console.log('setup')
const count = ref(0)
onBeforeMount(() => {
  let div = document.querySelector('#hello')
  console.log('创建之前===> onBeforeMount', div)
})
onMounted(() => {
  let div = document.querySelector('#hello')
  console.log('创建完成===> onMounted', div)
})
onBeforeUpdate(() => {
  console.log('更新之前===> onBeforeUpdate')
})
onUpdated(() => {
  console.log('更新完毕===> onUpdated')
})

</script>

<style scoped>
#hello {
  border: 1px solid #ccc;
}
</style>