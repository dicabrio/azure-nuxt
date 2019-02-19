<template>
  <form class="form-signin" @submit.prevent="submitForm">
    <div class="text-center mb-4">
      <img
        class="mb-4"
        src="https://getbootstrap.com/docs/4.0/assets/brand/bootstrap-solid.svg"
        alt
        width="72"
        height="72"
      >
      <h1 class="h3 mb-3 font-weight-normal">Floating labels</h1>
      <p>
        Build form controls with floating labels via the
        <code>:placeholder-shown</code> pseudo-element.
        <a
          href="https://caniuse.com/#feat=css-placeholder-shown"
        >Works in latest Chrome, Safari, and Firefox.</a>
      </p>
    </div>

    <div class="form-label-group">
      <input
        id="inputEmail"
        type="email"
        name="email"
        class="form-control"
        placeholder="Email address"
        v-model="username"
        v-validate="'required|email'"
        autofocus
      />
      <label for="inputEmail">Email address sdfsd</label>
    </div>
    <div class="text-danger">
      <span>{{ errors.first('email') }}</span>
    </div>

    <div class="form-label-group">
      <input
        id="inputPassword"
        type="password"
        class="form-control"
        placeholder="Password"
        v-model="password"
        required
      />
      <label for="inputPassword">Password</label>
    </div>

    <div class="checkbox mb-3">
      <label>
        <input type="checkbox" v-model="remember" /> Remember me
      </label>
    </div>
    <button class="btn btn-lg btn-primary btn-block" type="submit">Sign in</button>
    <p class="mt-5 mb-3 text-muted text-center">&copy; 2017-2018</p>
  </form>
</template>
<script>
export default {
  data() {
    return {
      username: '',
      password: '',
      remember: false
    }
  },
  methods: {
    submitForm(e) {
      window.console.log(this.username, this.password, this.remember)
    }
  }
}
</script>
