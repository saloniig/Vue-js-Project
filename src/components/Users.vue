<template>
	<div id="cube" >
		Enter No:<input type="number" id="number" ref="number" /><br />

		<p>
			<button v-on:click="getcube">Click Me!</button>
			<br />
      <br>Cube of Number is:
			{{ result }}
		</p>
	</div>
</template>
<script>
var cube = 0;
export default {
	data() {
		return {
			result: 0
		};
	},
	methods: {
		getcube: function() {
			cube = this.$refs.number.value;
			return (this.result = cube * cube * cube);
		}
	}
};
</script>

<style>
div{
  background-image:url('http://www.allwhitebackground.com/images/5/Light-Background-HD-Images.jpg');
}
</style>
