<script setup>
const props = defineProps({
  title: {
    type: String,
    default: "",
  },
  text: {
    type: String,
    default: "",
  },
  size: {
    type: String,
    default: "medium",
  },
  classModal: {
    type: String,
    default: "",
  }
});
</script>

<template>
  <transition name="fade">
    <div :class="classModal" class="modal">
      <div :class="size" class="modal__wrapper">
        <div class="modal__header">
          <h3 class="modal__title">{{ title }}</h3>
          <button class="modal__close"></button>
        </div>
        <div class="modal__body">
          <slot name="body">
            {{ text }}
          </slot>
        </div>
      </div>
    </div>
  </transition>
</template>

<style lang="scss" scoped>
.modal {
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  &__header {
    margin-bottom: 30px;
  }
  &__wrapper {
    position: relative;
    padding: 60px;    
    width: 95%;
    background-color: #f5f5f5;
    border-radius: 15px;
    &.small {
      max-width: 450px;
    }
    &.medium {
      max-width: 700px;
    }
  }
  &__close {
    position: absolute;
    top: 0;
    right: 0;    
    width: 48px;
    height: 48px;
    border-radius: 15px;
    background-color: #eaeef5;
    &:after {
      content: "";
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-45deg);
      width: 24px;
      height: 2px;
      background-color: #A0B846;
    }
    &:before {
      content: "";
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(45deg);
      width: 24px;
      height: 2px;
      background-color: #A0B846;
    }
  }
  &__title {
    font-family: "Nunito", sans-serif;
    text-align: center;
    font-weight: 500;
    font-size: 32px;
  }
}
</style>
