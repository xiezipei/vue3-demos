<template>
  <button @click="increment">+1</button>
  <div>当前todolist事项已有：{{ existCount }}条</div>
  <div>当前操作已新增：{{ count }}，共有{{ total }}条</div>
</template>

<script setup>
  import { ref, computed, onMounted } from 'vue'
  const count = ref(0)
  const existCount = ref(6)
  const total = computed(() => count.value + existCount.value)
  const increment = () => count.value++
  onMounted(() => console.log('component mounted!'))
</script>