<template>
  <div class="container">
    <div>
      <img src="https://flowbite.com/docs/images/logo.svg" alt="" />
      <span> Flowbite</span>
    </div>
    <div>
      <ul class="menu">
        <li>Home</li>
        <li>Company</li>
        <li>Team</li>
        <li>Contact</li>
      </ul>
    </div>
    <div>
      <button>Login</button>
      <button>sign up</button>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.container,
.menu {
  display: flex;
  justify-content: space-between;
}
li {
  list-style-type: none;
}
</style>