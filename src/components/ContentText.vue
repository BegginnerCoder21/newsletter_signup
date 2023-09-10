<template>
    <div class="mt-10 px-5 md:px-7">
        <h1 class="text-4xl font-bold">Stay updated!</h1>
        <p class="md:text-sm text-md text-gray-400 mt-4 md:mt-3">Join 60,000+ product managers receiving monthly updates on:</p>
        <ProductList />
        <Email />
        <SubmitButton>
            Subscribe to monthly newsletter
        </SubmitButton>
    </div>
</template>

<script setup lang="ts">
import ProductList from './ProductList.vue';
import Email from './Email.vue';
import SubmitButton from './SubmitButton.vue';


</script>

<style scoped>

</style>