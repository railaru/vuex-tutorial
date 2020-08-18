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

		};
	},
};
</script>

<style></style>
