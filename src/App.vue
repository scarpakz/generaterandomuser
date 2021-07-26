<template>
	<div class="main-container">
		<Header title="Users"/>
	</div>
</template>

<script>
import Header from './components/Header.vue'

export default {
	name: 'App',
	components:{
		Header,
	}
}
</script>

<style>
#app {
	font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
