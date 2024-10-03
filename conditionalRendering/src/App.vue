<script setup>
import { ref } from 'vue'

// V-if sẽ xóa/thêm mới phần tử vào DOM
// v-show thì sẽ ẩn hiện phần tử html bằng style css (display: none)
// v-if có thể dử dụng trong thẻ <template> còn v-show thì không

const isShow = ref(true)
const type = ref('A')
const isActive = ref(false)
const isTemplate = ref(false)
</script>

<template >
  <div>
    <h1 v-if="isShow">Hello World 1</h1>
    <h1 v-else>Hello World 2</h1>

    <div>
      <div v-if="type === 'A'">A</div>
      <div v-else-if="type === 'B'">B</div>
      <div v-else-if="type === 'C'">C</div>
      <div v-else>Not A/B/C</div>
    </div>

    <template v-if="isTemplate">
      <p v-show="isActive">Hiện thi bằng v-show: Window is active</p>
      <p v-if="isActive">Hiện thi bằng v-if: Window is active</p>
    </template>
  </div>
</template>

<style lang="scss">
</style>

