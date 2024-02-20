<template>
    <div>
        <Head>
            <Title>Nuxt Dojo | {{ item.title }}</Title>
            <Meta name="description" :content="item.description" />
        </Head>

        <ProductDetails :item="item" />
    </div>
</template>

<script setup>
    const { id } = useRoute().params;
    const uri = "https://fakestoreapi.com/products/" + id;

    //fetch data
    const { data: item } = await useFetch(uri, { key: id });

    if(!item.value) {
        throw createError({ statusCode: 404, statusMessage: "Product not found", fatal: true });
    };

    definePageMeta({
        layout: "products"
    });

</script>

<style scoped>

</style>