<template>
  <div :class="['flex flex-col h-screen', { 'index-layout': isIndexPage }]">

    <!-- Header -->
    <header v-if="isIndexPage" class="flex items-center justify-between px-8 py-4 custom-bg-color text-white">
      <!-- Hamburger Menu (Mobile Only) -->
      <button class="text-white focus:outline-none burger-menu" @click="toggleSideMenu">
        <svg class="w-6 h-6 fill-current" viewBox="0 0 24 24">
          <path v-if="!showSideMenu" d="M4 6h16M4 12h16M4 18h16" stroke="currentColor" stroke-width="2"
            stroke-linecap="round" stroke-linejoin="round" />
          <path v-else d="M6 18L18 6M6 6l12 12" stroke="currentColor" stroke-width="2" stroke-linecap="round"
            stroke-linejoin="round" />
        </svg>
      </button>
      <div class="flex items-center space-x-2 flex-grow justify-end">
        <img src="/images/user_icon.png" alt="User Icon" class="w-10 h-10 icon hidden md:block">
        <span class="text-lg font-medium text-right">Jessadakron Borisut</span>
      </div>
    </header>
    <!-- Main Content -->
    <main class="flex-1">
      <div class="flex h-screen">
        <!-- Side Menu -->
        <transition v-if="showSideMenu" name="slide">
          <SideMenu v-if="isIndexPage || showSideMenu" />
        </transition>

        <!-- Page Content -->
        <div class="flex-1 bg-gray-100">
          <div>
            <router-view></router-view>
          </div>
        </div>
      </div>
    </main>

    <!-- Footer -->
    <footer v-if="isIndexPage" class="px-4 py-2 custom-bg-color text-white">
      <div class="text-center">
        &copy; 2023 Integra8t. All rights reserved.
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
  data() {
    return {
      showSideMenu: false,
    };
  },
  computed: {
    isIndexPage() {
      return this.$route.path === '/' && !['/login', '/register'].includes(this.$route.path);
    },
  },
  methods: {
    toggleSideMenu() {
      this.showSideMenu = !this.showSideMenu;
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

.slide-enter-active,
.slide-leave-active {
  transition: transform 0.3s;
}

.slide-enter,
.slide-leave-to {
  transform: translateX(-100%);
}

@media (min-width: 768px) {

  .slide-enter,
  .slide-leave-to {
    transform: translateX(0);
  }

  /* Hide the burger menu in desktop mode */
  /* .burger-menu {
    display: none;
  } */

  /* Move the user icon to the left */
  .user-icon {
    order: -1;
  }
}

.custom-bg-color {
  background-color: #3C4B64;
}
</style>
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

.slide-enter-active,
.slide-leave-active {
  transition: transform 0.3s;
}

.slide-enter,
.slide-leave-to {
  transform: translateX(-100%);
}

@media (min-width: 768px) {

  .slide-enter,
  .slide-leave-to {
    transform: translateX(0);
  }

  /* Hide the burger menu in desktop mode */
  /* .burger-menu {
    display: none;
  } */

  /* Move the user icon to the left */
  .user-icon {
    order: -1;
  }
}

.custom-bg-color {
  background-color: #3C4B64;
}
</style>

