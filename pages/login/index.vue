<template>
  <div class="min-h-screen flex items-center justify-center bg-gradient-to-r from-blue-500 to-teal-500">
    <div class="max-w-md w-full p-6 bg-white rounded-lg shadow-md">
      <!-- <h2 class="text-3xl font-bold mb-6 text-center welcome-text">Integra8t</h2> -->
      <div class="logo-container">
        <img src="/images/int8_logo.png" alt="Int8 Logo" class="logo">
      </div>
      <div class="logo-container">
        <img src="/images/lms_logo.jpeg" alt="Oasis Logo" class="logo">
      </div>
      <LoginForm />
    </div>
  </div>
</template>

<script>
import LoginForm from '~/components/login/LoginForm.vue'

export default {
  components: {
    LoginForm
  }
}
</script>

<style>

.logo-container {
  display: flex;
  justify-content: center;
}

.logo {
  max-width: 200px;
  margin-bottom: 1rem;
}

.welcome-text {
  font-size: 2.5rem;
  color: white;
  background-color: #629baf;
  text-transform: uppercase;
  letter-spacing: 2px;
  padding: 1rem;
  margin-bottom: 2rem;
}
</style>
