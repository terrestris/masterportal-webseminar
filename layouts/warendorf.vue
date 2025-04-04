
<!-- default.vue -->
<template>
  <div class="slidev-layout default main">
    <img class="header-logo py-2" src="/warendorf_logo.png" />
    <slot />
    <!-- <div class="top-left-box" /> -->
    <!-- <div class="bottom-right-box" /> -->
  </div>
</template>

<style scoped>
.slidev-layout {
  padding-bottom: 0;
  padding-top: 1rem;
}

.header-logo {
  position: absolute;
  top: 0;
  right: 10px;
  width: 7rem;
}
.bottom-right-box {
  width: 2.5rem;
  height: 2.5rem;
  background: #19204c;
  position: absolute;
  right: 0;
  bottom: 0;
}
.top-left-box {
  width: 2.5rem;
  height: 2.5rem;
  background: #ffcc00ff;
  position: absolute;
  left: 0;
  top: 0;
}
</style>