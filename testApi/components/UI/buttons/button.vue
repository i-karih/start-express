<script setup>
const props = defineProps({
  label: {
    type: String,
    default: "Button",
  },
  type: {
    type: String,
    default: "primary",
  }
});
</script>

<template>
  <button :class="type" class="default-btn">{{ label }}</button>
</template>

<style lang="scss">
.default-btn {
  padding: 15px 34px;
  font-weight: 400;
  font-size: 14px;
  border: 1px solid transparent;
  &.primary {
    color: #13181b;
    background: #c37f53;
  }
  &.outline {
    color: #f0f0f0;
    background: transparent;
    border-color: #f0f0f0;
    &-orange {
        color: #13181b;
        border-color: #c37f53;
    }
  }
}
</style>
