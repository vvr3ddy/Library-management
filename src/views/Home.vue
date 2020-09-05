<template>

  <div class="home">
    <Navbar/>
    <JoinUS/>
  </div>
</template>

<script>
// @ is an alias to /src
import JoinUS from '@/components/JoinUS.vue'
import Navbar from '@/components/Navbar.vue'
export default {
  name: 'Home',
  components: {
    JoinUS,
    Navbar
  }
}
</script>
