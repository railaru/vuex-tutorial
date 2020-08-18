<template>
	<section>
		<h2>Product List One (Sale)</h2>
		<div :key="product.id" v-for="product in saleProducts">
			<table>
				<tr>
					<td><b>name:</b> {{ product.name }}</td>
					<td style="padding-left: 20px;">
						<b>price:</b> {{ product.price }}
					</td>
				</tr>
			</table>
		</div>
		<button @click="reducePrice">Reduce Price</button>
	</section>
</template>

<script>
export default {
	computed: {
		products() {
			return this.$store.state.products;
		},
		saleProducts() {
			return this.$store.getters.saleProducts;
		},
	},
	methods: {
		reducePrice() {
			this.$store.commit('reducePrice');
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

td {
	padding: 10px;
}
</style>
