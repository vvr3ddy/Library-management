<template>
  <div class="mt-5">
    <b-container fluid>
      <b-row>
        <b-col></b-col>
        <b-col cols="4">
          <p class="header">Join our community</p>
          <h1 class="join-us font-weight-bold">Create your account</h1>
          <div class="text-left">

            <label for="username-input" class="font-weight-bold">Username</label>  
            <b-form-input
              id="username-input"
              v-model="username"
              :state="usernameState"
              type="text"
              aria-describedby="username-feedback"
              trim>
            </b-form-input>
              <b-form-invalid-feedback id="username-feedback">
                Enter at least 6 letters
              </b-form-invalid-feedback>


            <label for="email-input" class="font-weight-bold">Email address</label>  
            <b-form-input
              id="email-input"
              v-model="email"
              :state="emailState"
              type="email"
              trim></b-form-input>
              <b-form-invalid-feedback id="email-feedback">
                Enter a valid email format
              </b-form-invalid-feedback>


          <label for="password-input" class="font-weight-bold">Password</label>  
            <b-form-input
              id="password-input"
              v-model="password"
              :state="passwordState"
              type="password"
              trim></b-form-input>
              <b-form-invalid-feedback id="password-feedback">
                Enter at least 8 letters
              </b-form-invalid-feedback>

          <vue-recaptcha sitekey="Site Key Here" :loadRecaptchaScript="true" class="mt-2"></vue-recaptcha>
          </div>
          <b-button variant="primary" class="signUp w-100" to="#" size="lg">Create account</b-button>
        </b-col>
        <b-col></b-col>
      </b-row>
    </b-container>
  </div>
</template>

<style>
.signUp{
  font-size: 14px;
  margin-top: 16px!important;
}
</style>

<script>
import VueRecaptcha from 'vue-recaptcha';
export default {
	data () {
		return {
			username: '',
			email: '',
			password: '',
			sitekey: '6LcFG8gZAAAAAAOMco4cNHuajCd1tBJvvXCxi1cI',
			form: {
				robot: false
			}
		}
	},
	methods: {
		submit: function () {
			if (this.form.robot) {

			}
		},
		onVerify: function (response) {
			if (response) this.form.robot = true;
		},
	},

	computed: {
		usernameState () {
			return this.username.length > 6 ? true : false
		}
	},
	components: {
		'vue-recaptcha': VueRecaptcha
	},
}
</script>