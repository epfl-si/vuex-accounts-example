<template>
<div>
  <form @submit.prevent="submitForm">
    <h3>Login</h3>
    <label>username</label>
    <input v-model="formData.username" />
    <label>password</label>
    <input v-model="formData.password" />
    <button>Login</button>
  </form>
</div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        username: '',
        password: ''
      }
    }
  },
  methods: {
    submitForm() {
      this.$store.dispatch('submitLoginForm', this.formData)
    }
  }
}
</script>
