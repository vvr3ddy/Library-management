<template>
  <b-container fluid>
    <div class="mt-5">
      <b-row>
        <b-col></b-col>
        <b-col cols="4">
          <div class="text-left">
            <p class="text-center">Join our community</p>
            <b-form @submit.stop.prevent="onSubmit">
              <b-form-group id="username-group" label="Username" label-for="username" class="font-weight-bold">
                <b-form-input
                  id="username"
                  name="username"
                  v-model="$v.form.username.$model"
                  :state="validateState('username')"
                  aria-describedby="username-feedback"
                ></b-form-input>

                <b-form-invalid-feedback
                  id="username-feedback"
                >This is a required field and must be at least 6 characters.</b-form-invalid-feedback>
              </b-form-group>

              <b-form-group id="email-group" label="Email" label-for="email" class="font-weight-bold">
                <b-form-input
                  id="email"
                  name="email"
                  v-model="$v.form.email.$model"
                  :state="validateState('email')"
                  aria-describedby="email-feedback"
                ></b-form-input>

                <b-form-invalid-feedback
                  id="email-feedback"
                >This is a required field and must be a valid email format.</b-form-invalid-feedback>
              </b-form-group>

              <b-form-group id="password-group" label="Password" label-for="password" class="font-weight-bold">
                <b-form-input
                  id="password"
                  name="password"
                  v-model="$v.form.password.$model"
                  :state="validateState('password')"
                  type=password
                  aria-describedby="password-feedback"
                ></b-form-input>

                <b-form-invalid-feedback
                  id="password-feedback"
                >This is a required field and must be atleast 8 characters.</b-form-invalid-feedback>
              </b-form-group>
              <div class='text-center'>
                <b-button class="mr-2" type="submit" variant="outline-success">Submit</b-button>
                <b-button class="ml-2" @click="resetForm()" variant="outline-danger">Reset</b-button>
              </div>
            </b-form>
          </div>
        </b-col>
        <b-col></b-col>
      </b-row>
    </div>
  </b-container>
</template>

<style>
body {
  padding: 1rem;
}
</style>

<script>
import { validationMixin } from "vuelidate";
import { required, email, minLength } from "vuelidate/lib/validators";

export default {
	mixins: [validationMixin],
	data () {
		return {
			form: {
				username: null,
				email: null,
				password: null
			}
		};
	},
	validations: {
		form: {
			username: {
				required,
				minLength: minLength(6)
			},
			email: {
				required,
				email
			},
			password: {
				required,
				minLength: minLength(8)
			}
		}
	},
	methods: {
		validateState (name) {
			const { $dirty, $error } = this.$v.form[name];
			return $dirty ? !$error : null;
		},
		resetForm () {
			this.form = {
				username: null,
				email: null,
				password: null
			};

			this.$nextTick(() => {
				this.$v.$reset();
			});
		},
		onSubmit () {
			this.$v.form.$touch();
			if (this.$v.form.$anyError) {
				return;
			}

			alert("Form submitted!");
		}
	}
};
</script>