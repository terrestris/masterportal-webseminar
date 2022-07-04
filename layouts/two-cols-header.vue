<!--
  Usage:

```md
---
layout: two-cols
---

# Left

This shows on the left

::right::

# Right

This shows on the right
```

-->

<script setup lang="ts">
const props = defineProps({
  class: {
    type: String,
  },
})
</script>

<template>
  <div>
    <div class="slidev-layout two-columns">
      <img class="header-logo py-2" src="/terrestris-logo-normal.svg" />
      <slot name="title" />
    </div>
    <div class="slidev-layout two-columns w-full h-full grid grid-cols-2">
      <div class="col-left" :class="props.class">
        <slot name="left"/>
      </div>
      <div class="col-right" :class="props.class">
        <slot name="right" />
      </div>
    </div>
  </div>
</template>

<style scoped>
  .slidev-layout.two-columns {
    padding-bottom: 0;
    padding-top: 1rem;
  }
  .header-logo {
    position: absolute;
    top: 0;
    right: 0;
    width: 9rem;
  }
</style>