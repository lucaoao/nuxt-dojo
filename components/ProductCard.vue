<template>
    <div class="card text-center">
        <img :src="item.image" alt="product photo" class="max-h-32 max-w-3/5 my-0 mx-auto">
        <p class="font-bold text-gray-500 m-4 truncate">{{ item.title }}</p>
        <NuxtLink :to="`/products/${item.id}`">
            <p class="btn my-4">View Details</p>
        </NuxtLink>
    </div>
</template>

<script setup>
    const { item } = defineProps(['item']);
</script>