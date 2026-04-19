<template>
  <div class="navbar">
    <div class="left">
      <div class="burger">
        <i class="mdi mdi-menu"></i>
      </div>
      <div class="branding-container">
        <img src="/logo.png" alt="Logo" class="logo" />
        <div class="vertical-divider"></div>
        <div class="branding-text-group">
          <h3 class="main-title">YOUTH</h3>
          <h6 class="sub-title">Project Management and Monitoring</h6> <!-- this could be a template -->
        </div>
      </div>
    </div>
    <div class="right">
      <i class="mdi mdi-moon-waning-crescent"></i> <!-- if else -->
      <div class="profile-container">
        <h4>Welcome Back,</h4>
        <h3></h3> <!-- detect user -->
      </div>
      <i class="mdi mdi-chevron-down"></i> <!-- on click -->
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.navbar {
  background-color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 24px 16px 24px;
}

.left, .right {
  display: flex;
  align-items: center;
  gap: 1rem;
}


.navbar-icon-container {
  width: 64px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-shrink: 0;
}

.branding-container {
  display: flex;
  align-items: center;
  gap: 10px;
}

.logo {
  height: 52px;
  width: auto;
}

.vertical-divider {
  width: 2.5px;
  height: 50px;
  background-color: #000;
}

.branding-text-group {
  display: flex;
  flex-direction: column;
  justify-content: center;
  line-height: 1.3;
}

.main-title {
  font-size: 22px;
  font-weight: 600;
  margin: 0;
  letter-spacing: -0.5px;
  color: #000;
}

.sub-title {
  font-size: 12px;
  font-weight: 500;
  margin: 0;
  color: #333;
  white-space: nowrap;
}
</style>