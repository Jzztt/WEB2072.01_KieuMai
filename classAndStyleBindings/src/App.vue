<script setup>
import { reactive, ref } from 'vue'
// 1. Class and Style Bindings
// class 2 binding : Object and Array
// :class="{box : isBox}"/ :class/ v-bind:attribute = key: value ( key = box, value = isBox)
// Nếu giá trị của key là true, thì sẽ add key vào trong class
const isBox = ref(true)
const classObject = reactive({
  button: true,
  active: true
})
const isDisabled = ref(true)
const isPrimary = ref(true)
const warning = ref('bg-danger')

const color = ref('red')
const textSuccess = ref('text-success')
const fontSize= ref(30)
</script>

<template>
  <div>
    <div>Hello World</div>
    <!-- <div :class="{box : isBox}" > Box</div> -->
    <button :class="[classObject, { primary: isPrimary }, textSuccess]" :disabled="isDisabled">
      Click
    </button>
    <p :style="{ color, fontSize : fontSize + 'px' }">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis quibusdam nam, recusandae
      laborum accusamus, neque ea eveniet voluptatum beatae, sunt eligendi minima. Obcaecati sunt
      accusantium sequi illo officiis saepe corporis?
    </p>
  </div>
</template>

<style lang="scss">
.box {
  width: 300px;
  height: 300px;
  background-color: Blue;
}
.button {
  background-color: #2d4ecf;
  color: white;
  border: 1px solid #2d4ecf;
  padding: 10px 14px;
  &:hover {
    background-color: #939dc2;
  }
}
.active {
  background-color: #3dd95c;
  color: white;
  &:hover {
    background-color: #81c987;
  }
}
.primary {
  background-color: #2d4ecf;
  color: white;
  &:hover {
    background-color: #939dc2;
  }
}
</style>

