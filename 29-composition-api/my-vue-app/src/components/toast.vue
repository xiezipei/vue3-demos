<template>
    <div>
        <button @click="showToast" class="btn">打开弹出</button>
        <teleport to="#teleportToast">
            <div v-if="toastFlag" class="toast__wrap" @click="hideToast">
                <h2>我是标题弹窗</h2>
                <div class="toast__wrap--msg">欢迎 {{ user }}，点击关闭</div>
            </div>
        </teleport>
    </div>
</template>

<script setup>
import { ref } from "vue";
defineProps({
  user: String
})
const toastFlag = ref(false)
const showToast = () => {
    toastFlag.value = true
}
const hideToast = () => {
    toastFlag.value = false
}
</script>

<style lang="scss">
.toast__wrap {
    position: fixed;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.8);
    top: 0;
    left: 0;
    z-index: 101;
    color: #fff;
    h2 {
        margin: 20px;
    }
    &--msg {
        text-align: center;
    }
}
</style>