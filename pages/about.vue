<template>
    <div>
        <h2>About</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Libero dignissimos atque doloremque nisi quo debitis incidunt in pariatur ipsum cumque?</p>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Libero dignissimos atque doloremque nisi quo debitis incidunt in pariatur ipsum cumque?</p>
        <div>{{ data }}</div>
    </div>
</template>

<script setup>
    const { data } = await useFetch('/api/nuxt-js-3?name=mario', {
        method: 'post', 
        body:{age:30}
    });
</script>

<style scoped>
h2{
    margin-bottom: 20px;
    font-size: 32px;
}

p{
    margin: 20px 0;
}

</style>