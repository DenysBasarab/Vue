<template>
  <div class="auth-page">
    <div class="container-page">
      <div class="row">
        <div class="col-md-6 offset-md-3 col-xs-12">
          <h1 class="text-xs-center">Sign Up</h1>
          <p class="text-xs-center">
            <router-link to="{name: login}">Need an account?</router-link>
          </p>
          VALIDATION ERRORS
          <form @submit.prevent="onSubmit">
            <fieldset class="form-group">
              <input
                type="text"
                class="form-control form-control-lg"
                placeholder="Username"
              />
            </fieldset>

            <fieldset class="form-group">
              <input
                type="text"
                class="form-control form-control-lg"
                placeholder="Email"
              />
            </fieldset>

            <fieldset class="form-group">
              <input
                type="password"
                class="form-control form-control-lg"
                placeholder="Password"
              />
            </fieldset>

            <button class="btn btn-lg btn-primary pull-xs-right">
              Sign Up
            </button>
          </form>
          <button @click="increaseCounter">Increase</button>
          {{ foo }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PageRegister',
  computed: {
    foo() {
      return this.$store.state.count
    }
  },
  methods: {
    onSubmit() {
      console.log('Submitted from')
    },
    increaseCounter() {
      console.log('increase counter')
      this.$store.commit('increment')
    }
  }
}
</script>

<style scoped></style>
