<template>
  <div>
    <input v-model="password"/>
    <p>{{ status }}</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      password: '',
      isWeak: true
    }
  },

  computed: {
    status () {
      return this.isWeak ? 'Weak' : 'Strong'
    }
  },

  watch: {
    password (newValue) {
      if ( newValue.length > 6 && /\d/.test(newValue) ) {
        this.isWeak = false
      } else {
        this.isWeak = true
      }
    }
  }
}
</script>
