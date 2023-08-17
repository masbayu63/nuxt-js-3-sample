<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="p in product"  :key="p.id">
                <ProductCard :product="p"/>
            </div>
        </div>
    </div>

</template>

<script setup>
    definePageMeta({
        layout:'products',
    })

    //fetch data
    const {data:product}= await useFetch('https://fakestoreapi.com/products')
    useHead({
        title:'Nuxt Practice | Merch',
        meta:[{
            name:'description', 
            content:'Nuxt 3 Practice | Merch',
        }]
    })
</script>

<style lang="scss" scoped>

</style>