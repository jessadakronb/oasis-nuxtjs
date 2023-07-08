<template>
  <div :class="['flex flex-col h-screen', { 'index-layout': isIndexPage }]">
    <!-- Header -->
    <header v-if="isIndexPage" class="flex items-center justify-end px-8 py-4 bg-gray-900 text-white">
      <div class="flex items-center space-x-2">
        <span class="text-lg font-medium">Jessadakron Borisut</span>
      </div>
    </header>

    <!-- Main Content -->
    <main class="flex-1">
      <div class="flex h-screen">
        <!-- Side Menu -->
        <SideMenu v-if="isIndexPage" />

        <!-- Page Content -->
        <div class="flex-1 bg-gray-100">
          <div>
            <router-view></router-view>
          </div>
        </div>
      </div>
    </main>

    <!-- Footer -->
    <footer v-if="isIndexPage" class="px-4 py-2 bg-gray-900 text-white">
      <div class="text-center">
        &copy; 2023 Your Company. All rights reserved.
      </div>
    </footer>
  </div>
</template>

<script>
import SideMenu from '@/components/SideMenu.vue';

export default {
  name: 'DefaultLayout',
  components: {
    SideMenu,
  },
  computed: {
    isIndexPage() {
      return this.$route.path === '/' && !['/login', '/register'].includes(this.$route.path);
    },
  },
};
</script>

<style scoped>
a {
  color: white;
}

a:hover {
  background-color: rgba(255, 255, 255, 0.1);
}

.index-layout {
  /* Custom styles for index page layout */
}
</style>
