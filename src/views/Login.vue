<template>
  <div class="mt-5">
    <b-container fluid>
      <b-row>
        <b-col></b-col>
        <b-col cols='3'>
          <p>Sign in to our Portal.</p>
          <b-card>
            <p class="text-left font-weight-bold uname">Username or email address</p>
            <b-field label="Email">
                    <b-input type="email"
                        placeholder=""
                        maxlength="50"
                        class="text-left">
                    </b-input>
            </b-field>
            <b-row>
              <b-col cols>
                <p class="text-left font-weight-bold password">Password</p>
              </b-col>
              <b-col cols>
                <p class="text-right forgotPassword">Forgot password?</p>
              </b-col>
            </b-row>
            <b-field label="Password">
                    <b-input type="password"
                        maxlength="32"
                        class="text-left">
                    </b-input>
            </b-field>
            <b-button variant="success" class="signin w-100">Sign in</b-button>
          </b-card>
          <b-card class="new-signup">
            <b-card-text>
              New to Portal? <a href="#">Create an account</a>
            </b-card-text>
          </b-card>
        </b-col>
        <b-col></b-col>
      </b-row>
    </b-container>
  </div>
</template>

<style>
.uname, .password, .forgotPassword{
  font-size: 14px;
  margin-top: 15px;
  margin-bottom:7px;
}
.signin{
  margin-top:10px;
}

.forgotPassword{
  cursor: pointer;
  color: blue;
}
.new-signup{
  margin-top: 15px;
  height: min-content;
}
</style>
