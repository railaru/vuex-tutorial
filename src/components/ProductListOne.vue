<template>
	<section>
		<h2>Product List One</h2>
		<ul>
			<li :key="product.id" v-for="product in products">
                {{ product.name }}
            </li>
		</ul>
	</section>
</template>

<script>
export default {
	props: {
		products: Array,
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
