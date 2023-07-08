<template>
  <div class="min-h-screen flex items-center justify-center bg-gradient-to-r from-blue-500 to-teal-500">
    <div class="max-w-md w-full p-6 bg-white rounded-lg shadow-md">
      <div class="logo-container">
        <img src="/images/int8_logo.png" alt="Int8 Logo" class="logo">
      </div>
      <RegisterForm />
    </div>
  </div>
</template>

<script>
import RegisterForm from '~/components/register/RegisterForm.vue'

export default {
  components: {
    RegisterForm
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

</style>
