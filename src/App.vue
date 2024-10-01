<script>
import AppHeader from './components/Header/AppHeader.vue';
import AppMain from './components/Main/AppMain.vue';
import AppFooter from './components/Footer/AppFooter.vue';

export default {
		name: 'App',
  		components : {
			AppHeader,
			AppMain,
			AppFooter
  	}
  }
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
  <AppFooter></AppFooter>
</template>


<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,400;0,500;0,700;1,400;1,500;1,700&display=swap');
	@import "styles/main";
	@import "./styles/main.scss";

    body {
		font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
	}

</style>