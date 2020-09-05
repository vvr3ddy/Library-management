<template>
<div>
  
  <b-navbar toggleable="sm" type="dark" variant="dark">
    <b-navbar-brand href="#">Library</b-navbar-brand>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
    
    <!--Add Elements to the right hand side of Nav Bar  -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item to="/">Home</b-nav-item>
        <b-nav-item to="/login">Login</b-nav-item>
        <b-nav-item to="/join">Signup</b-nav-item>
      </b-navbar-nav>
    
    </b-collapse>
  </b-navbar>
</div>  
</template>


