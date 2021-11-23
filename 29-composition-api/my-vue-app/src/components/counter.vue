<script setup>
import { ref, computed, onMounted, toRefs, watch } from 'vue'

  // ref响应式变量
    const count = ref(0)
    const existCount = ref(6)
    // computed方法，在count的value发生改变时，会触发计算total
    const total = computed(() => count.value + existCount.value )
    function increment() {
      count.value++
    }
    
    onMounted(() => console.log('component mounted!'))

</script>

<template>
  <button @click="increment">+1</button>
  <div>当前todolist事项已有：{{ existCount }}条</div>
  <div>当前操作已新增：{{ count }}，共有{{ total }}条</div>
</template>

<style>

</style>