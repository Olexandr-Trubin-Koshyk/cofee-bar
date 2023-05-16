<template>
  <header class="header">
    <div class="header__logo">
      <svg width="48" height="48"></svg>
    </div>
    <nav class="header__nav">
      <ul class="header__navList">
        <li>Menu</li>
        <li>About us</li>
        <li>Contacts</li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
export default {};
</script>

<style lang="scss">
.header {
  display: flex;
  justify-content: space-between;
  background-color: black;
}

.header__logo {
  background: url("../assets/main-logo.svg");
  background-size: 48px;
  background-repeat: no-repeat;
  background-position: center;
  padding: 12px 24px;
  cursor: pointer;
}

.header__nav {
  padding: 12px 24px;
}

.header__navList {
  display: flex;
  gap: 24px;
}
</style>
