<template>
  <div id="app">
    <!-- <twitter-input /> -->
    <password-input />
  </div>
</template>

<script>
import TwitterInput from './components/TwitterInput.vue'
import PasswordInput from './components/PasswordInput.vue'

export default {
  name: 'app',
  components: {
    TwitterInput,
    PasswordInput
  }
}
</script>
