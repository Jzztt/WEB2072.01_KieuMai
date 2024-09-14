<script setup>
import { nextTick } from 'vue';
import { ref, reactive } from 'vue'
var count = ref(0) // {value: 1}
// Bước 1: theo dõi giá trị thay đổi
// Bước 2: cập nhật lại DOM, cập nhật template

// trong Javascript có những kiểu dữ liệu nào
// Kiểu dữ liệu đơn giản : number, string, boolean, null, undefined, symbol
// Kiểu dữ liệu phức tạp: Object, array, function

const increment = () =>{
  count.value++;
  console.log(count.value);
}

// 2. Deep Reactivity
const user = ref({
  name: 'John',
  age: 30,
  hobbies: {
    name: 'cooking',
    time: 5
  }
})

const handleChangeNameHobbies = () =>{
  user.value.hobbies.name = 'running';
}

// 3. Reactive
const price = reactive({count: 0})

const incrementReactive = async () =>{
  price.count++;
  console.log("step 1:",document.getElementById('price').innerText);
  //4. NextTick()
  await nextTick()
  console.log("step 2:",document.getElementById('price').innerText);

}
</script>
<template>
  <div>
    <div>
      <h3> Tìm hiểu về Ref</h3>
      <div>{{ count }}</div>
      <button @click="increment">Count</button>
    </div>
    <div>
      <h3> Tìm hiểu về Deep Reactivity</h3>
      <div>{{ user.name }}, {{ user.age }}</div>
      <div>{{user.hobbies.name}}, {{user.hobbies.time}}</div>
      <button @click="handleChangeNameHobbies">Change Name</button>
    </div>
    <div>
      <h3> Tìm hiểu về Reactive</h3>
      <div id="price">{{ price.count }}</div>
      <button @click="incrementReactive">Count</button>
    </div>
  </div>
</template>

<style>
</style>

