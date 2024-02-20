<template>
    <div class="card">
        <div class="grid grid-cols-2 gap-10">
            <div class="p-7">
                <img :src="item.image" alt="product image" class="mx-auto my-7 max-w-md" />
            </div>
            <div class="p-7">
                <h2 class="text-4x1 my-7">{{ item.title }}</h2>
                <p class="text-xl my-7">Price: ${{ item.price }}</p>
                <h3 class="font-bold border-b-2 mb-2 pb-2">Product description: </h3>
                <p class="mb-7">{{ item.description }}</p>
                <button class="btn flex">
                    <i class="material-icons mr-2">add_shopping_cart</i>
                    <span>Add to cart</span>
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>
    const { item } = defineProps(['item']);

</script>