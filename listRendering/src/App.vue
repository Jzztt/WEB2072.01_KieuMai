<script setup>
import { reactive } from 'vue'

// Tạo 1 biến product là 1 mảng chứa 2 đối tượng sản phẩm điện thoại
// có thuộc tính name và price

const products = reactive([
  { name: 'Iphone 16 pro', price: 1000 },
  { name: 'Galaxy s22 unltra', price: 2000 }
])

// Tạo 1 biến foods là reactive 1 mảng chứa  các giá trị "rice", "beef", "chicken".
// Hãy in ra ngoài màn hình các giá trị trong mảng

const foods = reactive(['rice', 'beef', 'chicken'])

const users = reactive([
  {
    id: 1,
    name: 'John',
    address: '123 Main St',
    isActive: true
  },
  {
    id: 2,
    name: 'Jane',
    address: '456 Elm St',
    isActive: false
  },
  {
    id: 3,
    name: 'Bob',
    address: '789 Oak St',
    isActive: true
  }
])
</script>

<template>
  <div>
    <h1>Hello World</h1>
    <ul>
      <li v-for="(food, index) in foods" :key="index">
        {{ food }}
      </li>
    </ul>
    <ul>
      <li v-for="product in products" :key="product.name">
        {{ product.name }} - {{ product.price }}
      </li>
    </ul>

    <ul>
      <template v-for="user in users">
        <li id="user" v-if="user.isActive" :key="user.id">
          {{ user.name }} - {{ user.address }} - {{ user.isActive ? 'Active' : 'Inactive' }}
        </li>
      </template>
    </ul>
  </div>
</template>

<style>
</style>
