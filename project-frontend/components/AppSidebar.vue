<template>
  <aside class="sidebar">
    <NuxtLink
      v-for="navRoute in navigationRoutes"
      :key="navRoute.path"
      :to="navRoute.path"
      class="sidebar-item"
      active-class="sidebar-item--active"
    >
        <span :class="`mdi ${navRoute.meta.icon} sidebar-icon`"></span>
        <span class="sidebar-title">{{ navRoute.meta.title }}</span>
    </NuxtLink>
  </aside>
</template>

<script setup>
import { navigationRoutes } from '@/config/navigation'

const route = useRoute()

const isOpen = ref(true)

const isRouteActive = (navRoute) => {
    return route.path === navRoute.path || route.path.startsWith(navRoute.path + '/')
}
</script>

<style scoped>
.sidebar {
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 240px;
  background: #fff;
  padding: 10px;
  gap: 0.5rem;
}

.sidebar-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 12px;
  border-radius: 8px;
  font-size: 15.5px;
  font-weight: 500;
  text-decoration: none;
  color: inherit;
  transition: all 0.2s ease;
}

.sidebar-item:hover {
  background: rgba(0, 0, 0, 0.04);
}

.sidebar-item--active {
  background: #174499;
  color: white;
  box-shadow: 0 4px 8px rgba(23, 68, 153, 0.15);
  font-weight: 700;
}

.sidebar-item--active:hover {
  background: #447be2;
}
</style>
