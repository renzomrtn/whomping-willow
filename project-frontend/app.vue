<template>
  <div class="app-layout">
    <AppHeader />
    <div class="content-area">
      <AppSidebar />

      <div class="main-content">
        <main>
          <NuxtPage />
        </main>
      </div>
    </div>
  </div>
</template>

<style>
.app-layout {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

.content-area {
  display: flex;
  flex: 1;
  overflow: hidden;
}

.main-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

main {
  flex: 1;
  overflow-y: auto;
  background-color: #f3f3f3;
  border-radius: 28px 0 0 0;
}
</style>