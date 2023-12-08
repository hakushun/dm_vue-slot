<template>
  <div :class="styles.root">
    <slot name="header" />
    <slot name="body" />
    <slot name="footer" />
  </div>
</template>

<style module="styles">
.root {
  display: flex;
  flex-direction: column;
  width: 300px;
  padding: 32px;
  background-color: lightyellow;
  border-radius: 6px;
}
</style>
