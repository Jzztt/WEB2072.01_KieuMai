<script setup>
// 1. Text Interpolation
const title = 'template syntax'
// cứ pháp khởi tạo biến  + tên biến = giá trị

// 2. Raw HTML
const content = '<span style="color:red">RawHTML</span>'

// 3. Attribute Bindings and short-hand
const linkGG = 'https://google.com'
const fullName = 'name'
// v-bind ( cú pháp truyền dữ liệu) + : + thuộc tính = tên biến
//: + thuộc tính = tên biến

// 4. Boolean Attributes
const isClick = false;


// 5.Dynamically Binding Multiple Attributes
// Truyền nhiều thuộc tính dữ liệu
const box = {
  id: 'box',
  style: 'width:100px; padding:10px',
  class: 'box-group'
}

// Bài tập: tạo  object chứ các thuộc tinh id, class, style
// yêu cầu tạo 1 ra box với width, height 300px, border 1px solid
// truyền  toàn bộ thuộc tính đấy vào 1 thẻ div
</script>

<template>
  <div>
    <div>{{ title }}</div>
    <div id="content" v-html="content"></div>
    <a v-bind:href="linkGG">Google</a>
    <p :id="fullName">Lê văn Hiển</p>
    <p>{{ isClick ? 'Yes' : 'No' }}</p>
    <button :disabled="isClick">Click</button>
    <div v-bind="box">Hello</div>
  </div>

</template>

<style>
#name {
  color:yellow
}
</style>

