<template>
  <a class="VPNavBarTitle" href="/">
    <slot name="navbar-title">
      <span class="text">Cocos Cheat Book</span>
    </slot>
  </a>
</template>

<style scoped>
.bevy_logo {
  height: 32px;
  width: 140px;
}
.VPNavBarTitle {
  display: flex;
  align-items: center;
  padding-top: 1px;
  height: var(--vt-nav-height);
  transition: opacity 0.25s;
}

.VPNavBarTitle:hover {
  opacity: 0.6;
}

.logo {
  position: relative;
}

.logo+.text {
  padding-left: 8px;
}

.text {
  font-size: 16px;
  font-weight: 500;
}
</style>
