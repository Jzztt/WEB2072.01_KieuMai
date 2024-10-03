<template>
    <div class="container">
    <h3 class="text-center mt-5">Form Input Binding</h3>
    <div class="w-50 m-auto border p-4 rounded shadow">
      <form>
        <div class="form-group mb-2">
          <label class="d-block mb-1" for="email"> Email</label>
          <input type="text" id="email" class="form-control" v-model="infoLogin.email" />
        </div>
        <div class="form-group mb-2">
          <label class="d-block mb-1" for="password">Password </label>
          <input type="text" id="password " class="form-control" v-model="infoLogin.password" />
        </div>
        <button type="submit" class="mt-2 btn btn-primary" @click.prevent="handleLogin">
          Login
        </button>
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const infoLogin = ref({
  email: '',
  password: ''
})
const handleLogin = () => {
  console.log('email:', infoLogin.value.email)
  console.log('password', infoLogin.value.password)
}

</script>

<style lang="scss" scoped>

</style>