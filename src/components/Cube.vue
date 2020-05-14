<template>
	<div id="cube" >
		Enter No:<br />
	<input type="text" class="textfield" @keypress="isNumber($event)" id="number" ref="number" />
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
		isNumber: function(evt) {
      evt = (evt) ? evt : window.event;
      var charCode = (evt.which) ? evt.which : evt.keyCode;
      if ((charCode > 31 && (charCode < 48 || charCode > 57)) && charCode !== 46) {
        evt.preventDefault();
		alert('Enter number only');
      } else {
        return true;
      }
    },
		getcube: function() {
			cube = this.$refs.number.value;
			return (this.result = cube * cube * cube);
		}
	}
};
</script>

<style>

</style>
