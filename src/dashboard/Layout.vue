<template>
  <dashboard-provider>
    <div class="bg-body h-screen overflow-hidden relative">
      <div class="flex items-start">
        <Overlay />
        <side-navigation mobile-position="right" />
        <div class="flex flex-col h-screen pl-0 w-full lg:space-y-4 lg:w-99">
          <top-navigation />
          <main
            class="
              h-screen
              overflow-auto
              pb-36
              pt-8
              px-2
              md:pb-8 md:pt-4 md:px-8
              lg:pt-0
            "
          >
            <slot />
          </main>
        </div>
      </div>
    </div>
  </dashboard-provider>
</template>

<script setup>
import Overlay from './provider/Overlay.vue';
import TopNavigation from './topnavigation/Index.vue';
import SideNavigation from './sidenavigation/Index.vue';
import DashboardProvider from './provider/Provider.vue';
</script>
