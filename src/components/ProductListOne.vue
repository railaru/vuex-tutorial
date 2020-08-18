<template>
	<section>
		<h2>Product List One</h2>
		<div :key="product.id" v-for="product in products">
			<table>
				<tr>
					<td><b>name:</b> {{ product.name }}</td>
					<td style="padding-left: 20px;"><b>price:</b> {{ product.price }}</td>
				</tr>
			</table>
		</div>
	</section>
</template>

<script>
export default {
	computed: {
		products() {
			return this.$store.state.products;
		},
	},
};
</script>

<style scoped>
section {
	padding: 20px;
	background: rgb(238, 238, 137);
}

ul {
	display: grid;
	grid-template-columns: 1fr 1fr;
	grid-gap: 20px;
}
</style>
