<template>
  <div class="app-layout">
    <AppSidebar />
    <div class="main-content">
      <AppHeader />
      <main>
        <NuxtPage />
      </main>
    </div>
  </div>
</template>

<style>
.app-layout {
  display: flex;
  height: 100vh;
}

.main-content {
  flex: 1;          /* takes up remaining space */
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

main {
  flex: 1;
  overflow-y: auto; /* scroll only the content, not the whole page */
  height: 100%;
  background-color: #f3f3f3;
  border-radius: 28px;
  border: 1px solid red;
}
</style>