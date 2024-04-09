<script setup> 
import usersMixin from './mixins/users.js'
import AuthModal from './components/modals/auth-modal.vue'

const test1 = ref('')
const test2 = ref('')

const auth = () => {
  console.log(usersMixin);
}
</script>

<template>
  <div>
    <h1>Test Api</h1>    
    <AuthModal/>
  </div>
</template>

<style lang="scss">
  h1 {
    color: blue;
  }
</style>
