<template>
  <div>
    <form class="space-y-4">
      <div>
        <label class="block" for="firstName">ชื่อ (First Name):</label>
        <input id="firstName"
          class="w-full px-3 py-2 text-gray-700 border rounded-lg focus:outline-none focus:shadow-outline" type="text"
          placeholder="Enter your first name">
      </div>
      <div>
        <label class="block" for="lastName">นามสกุล (Last Name):</label>
        <input id="lastName"
          class="w-full px-3 py-2 text-gray-700 border rounded-lg focus:outline-none focus:shadow-outline" type="text"
          placeholder="Enter your last name">
      </div>
      <div>
        <label class="block" for="username">ชื่อผู้ใช้ (Username):</label>
        <input id="username"
          class="w-full px-3 py-2 text-gray-700 border rounded-lg focus:outline-none focus:shadow-outline" type="text"
          placeholder="Enter your username">
      </div>
      <div>
        <label class="block" for="email">อีเมล (Email):</label>
        <input id="email" class="w-full px-3 py-2 text-gray-700 border rounded-lg focus:outline-none focus:shadow-outline"
          type="email" placeholder="Enter your email">
      </div>
      <div>
        <label class="block" for="password">รหัสผ่าน (Password):</label>
        <input id="password"
          class="w-full px-3 py-2 text-gray-700 border rounded-lg focus:outline-none focus:shadow-outline" type="password"
          placeholder="Enter your password">
      </div>
      <div>
        <label class="block" for="confirmPassword">ยืนยันรหัสผ่าน (Confirm Password):</label>
        <input id="confirmPassword"
          class="w-full px-3 py-2 text-gray-700 border rounded-lg focus:outline-none focus:shadow-outline" type="password"
          placeholder="Confirm your password">
      </div>
      <div>
        <label class="block" for="phone">เบอร์โทรศัพท์ (Phone Number):</label>
        <input id="phone" class="w-full px-3 py-2 text-gray-700 border rounded-lg focus:outline-none focus:shadow-outline"
          type="tel" placeholder="Enter your phone number">
      </div>
      <div>
        <button
          class="w-full px-4 py-2 text-white font-semibold bg-blue-500 rounded-lg hover:bg-blue-600 focus:outline-none focus:shadow-outline"
          type="submit">Create an Account</button>
      </div>
    </form>
  </div>
</template>
