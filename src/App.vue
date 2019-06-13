<template>
	<div id="app">
		<div v-show="!isLoad">加载</div>
		<router-view v-show="isLoad"/>
	</div>
</template>
<script>
export default {
	data() {
		return {
			isLoad:false
		}
	},
	mounted() {
		this.$nextTick(()=>{
			setTimeout(() => {
				this.isLoad = true ;
			}, 1000);
		})
	},
}
</script>
<style lang="scss" scoped>
#app {
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
}
</style>
