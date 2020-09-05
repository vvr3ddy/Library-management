<template>
  <div>
    
    <b-row class="mt-5">
    <b-col></b-col>
    <b-col cols="4" class="text-left mt-5">
      <h1 class="font-weight-bold ">Built with ❤️ for</h1>
      <h1 class="font-weight-bold">Book Lovers</h1>
      <p class="text-justify">Access thousands of books across tens of genres at your fingertips.</p>
    </b-col>
    <b-col cols="4">
      <b-card>
        <h6 class="text-left font-weight-bold uName">Username</h6>
        <b-form-input type="name"></b-form-input>
        <h6 class="text-left font-weight-bold eMail">Email</h6>
        <b-form-input type="email"></b-form-input>
        <h6 class="text-left font-weight-bold pwd" type="email">Password</h6>
        <b-form-input type="password"></b-form-input>
        <b-button variant="success" class="signUp" to="#">Sign Up</b-button>

      </b-card>
    </b-col>
    <b-col></b-col>
    </b-row>
  </div>
</template>

<style>
.uName, .eMail, .pwd, .signUp {
  margin-top: 10px;
  font-size: 14px;
}
</style>
