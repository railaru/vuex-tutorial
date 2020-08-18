<template>
	<div id="app">
		<ProductListOne :products="products" />
		<ProductListTwo :products="products" />
	</div>
</template>

<script>
import ProductListOne from './components/ProductListOne';
import ProductListTwo from './components/ProductListTwo';

export default {
	name: 'App',
	components: { ProductListOne, ProductListTwo },
	data() {
		return {
			products: [
				{ id: 0, name: 'Banana Skin', price: 20 },
				{ id: 1, name: 'Shiny Star', price: 40 },
				{ id: 2, name: 'Green Shells', price: 60 },
				{ id: 3, name: 'Red Shells', price: 80 },
			],
		};
	},
};
</script>

<style></style>
