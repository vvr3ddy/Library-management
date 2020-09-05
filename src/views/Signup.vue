<template>
  <div class="mt-5">
    <b-container fluid>
      <b-row>
        <b-col></b-col>
        <b-col cols="4">
          <p class="header">Join our community</p>
          <h1 class="join-us font-weight-bold">Create your account</h1>
          <div class="text-left">
          <p class="font-weight-bold">Username <span class="text-danger">*</span></p>
          <b-form-input type="name"></b-form-input>
          <p class="font-weight-bold">Email address <span class="text-danger">*</span></p>
          <b-form-input type="email"></b-form-input>
          <p class="font-weight-bold">Password <span class="text-danger">*</span></p>
          <b-form-input type="password"></b-form-input>
          <vue-recaptcha sitekey="6LcFG8gZAAAAAAOMco4cNHuajCd1tBJvvXCxi1cI" :loadRecaptchaScript="true" class="mt-2"></vue-recaptcha>
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
	components: {
		'vue-recaptcha': VueRecaptcha
	},
}
</script>