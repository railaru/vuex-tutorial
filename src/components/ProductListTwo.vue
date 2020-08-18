<template>
	<section>
		<h2>Product List Two</h2>
		<ul>
			<li :key="product.id" v-for="product in saleProducts">
				{{ product.name }}
				{{ product.price }}
			</li>
		</ul>
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
};
</script>

<style scoped>
section {
	padding: 20px;
	background: rgb(140, 238, 137);
}
</style>
