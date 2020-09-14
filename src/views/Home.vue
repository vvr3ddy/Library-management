<template>

  <div class="home">
    <Navbar/>
    <JoinUS/>
  </div>
</template>

<script>
// @ is an alias to /src
import JoinUS from '@/views/JoinUS.vue'
import Navbar from '@/components/Navbar_Gen.vue'
export default {
	name: 'Home',
	components: {
		JoinUS,
		Navbar
	}
}
</script>
