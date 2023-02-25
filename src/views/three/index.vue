<!--
 * @Author: DaiYu
 * @Date: 2023-02-23 11:24:01
 * @LastEditors: DaiYu
 * @LastEditTime: 2023-02-23 16:19:49
 * @FilePath: \src\views\three\index.vue
 * @Description: file content
-->
<template>
  <div>
    <canvas ref="canvas" class="webgl"></canvas>
  </div>
</template>

<script lang="ts" setup name="">
import * as THREE from 'three'

// 1.初始化渲染器
const canvas = ref<Nullable<HTMLCanvasElement>>(null)
let scene = ref(null)
onMounted(() => {
  console.log(canvas.value)
  initScene()
})
function initScene() {
  scene.value = new THREE.Scene()
}
</script>
<style lang="less" scoped></style>
