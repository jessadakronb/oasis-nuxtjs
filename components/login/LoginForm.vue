<template>
  <form class="space-y-4">
    <div>
      <label class="block text-sm font-medium text-gray-700" for="email">Email</label>
      <input id="email" class="w-full px-3 py-2 text-gray-700 border rounded-lg focus:outline-none focus:shadow-outline"
        type="email" placeholder="Enter your email">
    </div>
    <div>
      <label class="block text-sm font-medium text-gray-700" for="password">Password</label>
      <input id="password"
        class="w-full px-3 py-2 text-gray-700 border rounded-lg focus:outline-none focus:shadow-outline" type="password"
        placeholder="Enter your password">
    </div>
    <div class="flex justify-end items-center">
      <a class="text-sm text-gray-600 hover:text-gray-800 mr-2" href="/forgot-password">
        Forgot Password?
      </a>
    </div>
    <div>
      <button
        class="w-full px-4 py-2 text-white font-semibold bg-teal-500 rounded-lg hover:bg-teal-600 focus:outline-none focus:shadow-outline"
        type="submit">Sign In</button>
    </div>
    <div>
      <button
        class="w-full px-4 py-2 text-white font-semibold bg-blue-500 rounded-lg hover:bg-blue-600 focus:outline-none focus:shadow-outline"
        type="submit">Create an Account</button>
    </div>
  </form>
</template>
