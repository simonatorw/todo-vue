<template>
	<div class="hello">
		<form v-on:submit="addItem">
			<h1>{{msg}}</h1>
			<input type="text" v-model="newItem">
			<ul>
				<li v-for="(item, index) in list" v-on:click="remove(index)">{{item}}</li>
			</ul>
		</form>
	</div>
</template>

<script>
	export default {
		name: 'HelloWorld',
		data () {
			return {
				msg: 'To-Do List',
				newItem: '',
				list: [
					'foo',
					'bar'
				]
			};
		},
		methods: {
			addItem: function (e) {
				e.preventDefault();
				if (this.newItem) {
					console.log(this.newItem);
					this.list.push(this.newItem);
					this.newItem = '';
				}
			},
			remove: function (i) {
				this.list.splice(i, 1);
			}
		}
	};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	h1, h2 {
		font-weight: normal;
	}
	ul {
		padding: 0;
	}
	li {
		margin: 0 10px;
		cursor: pointer;
	}
	a {
		color: #42b983;
	}
</style>
