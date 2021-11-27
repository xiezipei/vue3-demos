<template>
  <div>
    <div>count:{{ count }},msg:{{ info }}</div>
    <button @click="incAndChangeInfo">
      增加 1修改msg
    </button>
  </div>
  
</template>
<script setup>
  import { ref } from 'vue'
  const prop = defineProps({
      msg: String
  })
  const count = ref(0)
  const info = ref(prop.msg)
  const incAndChangeInfo = () => {
    count.value++
    info.value = "change hello" + count.value
  }
</script>