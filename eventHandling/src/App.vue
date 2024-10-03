<script setup>
import { nextTick, ref } from 'vue'

// 1. Event Handling
const count = ref(0)
const name = ref('Le Van Hien')

const handleCount = () => {
  count.value++
}
const handleShowName = (name) => {
  alert('Your Name: ' + name)
}
const handleMouseUp = (e, name) => {
  console.log([e.target])
}

// Button có 1 sự kiện click. Khi click hiện thị alert Hello Tên của bạn
// Tạo 1 sự kiện mouseup tên là handleMousseUp nhận vào tham số content có dối số la param . Thực thi 1 hàm console.log ra param
</script>

<template>
  <div>
    <p>{{ count }}</p>
    <button @click="handleCount">Count</button>
    <button @click="handleShowName(name)">Show Name</button>
    <div>
      <button
        @click="console.log('click')"
        @mousedown="console.log('mousedown')"
        @mouseup="console.log('mouseup')"
      >
        Check mouse event
      </button>
    </div>
    <div>
      <button @click.stop="console.log('button1')">
        Button1
        <button @click.stop="console.log('button2')">Button2</button>
      </button>
    </div>
    <div>
      <form @submit.prevent="console.log('submit')">
        <input type="text" @keyup.enter="console.log('KeyUp')" />
        <button type="submit">Submit</button>
      </form>
    </div>
    <div>

    </div>
  </div>
</template>

<style scoped>
</style>
