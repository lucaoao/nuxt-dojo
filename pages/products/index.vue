<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="item in products">
                <ProductCard :item="item" :loading="loading"/>
            </div>
        </div>
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'products'
    });

    const loading = ref();

    // fetch products
    const { data: products } = await useFetch("https://fakestoreapi.com/products/");



    useHead({
        title: "Nuxt Dojo | Merch",
        meta: [
            { name: "description", content: "Nuxt is fun." },
        ],
    });
</script>

<style scoped>

</style>