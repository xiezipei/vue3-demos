<template>
  <div class="my-vue-app">
    <h1>Vue 3 App</h1>
    <!-- 示例 1 s -->
    <div class="section">
      <h2>1. Composition API（组合式 API）</h2>
      <div class="desc">
        Vue2.X 基于 Option API（选项 API）构建组件，一般来说组件拥有 data、methods、computed 等选项。这是一种属性相互隔离的模式，好处是各属性内容分离开，对于新手来说比较友好；但对于大型项目来说，为了修改某个功能，可能需要在一个文件中来回翻页。Vue3 增加了 Composition API 方式（组合 API ），基于 reactivity（响应式）的思想进行组件构建，将逻辑封装到函数中，可以实现类似 ReactHooks 的逻辑组合和重用。
      </div>
      <counter />
    </div>
    <!-- 示例 1 e -->
    <!-- 示例 2 s -->
    <div class="section">
      <h2>2. Teleport（传入）</h2>
      <div class="desc">
        Teleport 功能，使得我们可以将全屏的组件（例如 Toast）移到 Vue APP 节点外，而不需要在 UI 界面上修改其他组件样式，方便实现全屏蒙层、浮层弹窗等效果。
      </div>
      <toast :user="'xxx'" />
    </div>
    <!-- 示例 2 e -->
    <!-- 示例 3 s -->
    <div class="section">
      <h2>3. Fragments（碎片）</h2>
    </div>
    <!-- 示例 3 e -->
    <!-- 示例 4 s -->
     <div class="section">
      <h2>4. 语法糖 script setup、style vars</h2>
    </div>
  </div>
</template>

<script setup>
  import counter from "./components/counter.vue"
  import toast from "./components/toast.vue"
</script>

<style lang="scss">
.my-vue-app {
  width: 100%;
  box-sizing: border-box;
  padding: 0 24px 24px;
  .section {
    border: 1px solid #ccc;
    padding: 0 24px 24px;
    margin-bottom: 24px;
    .desc {
      margin-bottom: 16px;
      font-size: 14px;
      color: #666;
    }
  }
}
</style>
