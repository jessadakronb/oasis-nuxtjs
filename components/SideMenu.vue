<template>
  <div class="w-64 custom-bg-color text-white">
    <!-- Logo -->
    <div class="flex items-center justify-center py-4 ">
      <img src="/images/int8_logo2.png" alt="Int8 Logo" class="logo">
    </div>
    <hr />
    <br />
    <!-- Menu Items -->
    <nav>
      <ul class="space-y-2">
        <li>
          <router-link to="/" class="block px-4 py-2 hover:bg-gray-800">หน้าหลัก</router-link>
        </li>
        <li>
          <router-link to="/leave-request" class="block px-4 py-2 hover:bg-gray-800">วันหยุดประจำปี</router-link>
        </li>
        <li>
          <router-link to="/leave-history" class="block px-4 py-2 hover:bg-gray-800">เพิ่มบันทึกการลา</router-link>
        </li>
        <li>
          <router-link to="/leave-management" class="block px-4 py-2 hover:bg-gray-800">ข้อมูลบัญชี</router-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'SideMenu',
};
</script>

<style scoped>
.logo {
  max-width: 160px;
  margin-bottom: 1rem;
}

.custom-bg-color {
  background-color: #3C4B64;
}
</style>
