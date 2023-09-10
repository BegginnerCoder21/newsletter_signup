<template>
    <div>
        <ul class="mt-2">
            <li v-for="product in listproduct" class="flex md:items-center mt-3 space-y-3 md:space-y-2 space-x-1">
                <img src="../assets/images/icon-success.svg" alt="" class="w-4 h-4 flex items-center mt-[16px] md:mt-2">
                <span class="md:text-xs text-sm">{{ product }}</span> 
            </li>
        </ul>
    </div>
</template>

<script setup lang="ts">

const listproduct = [
    'Product discovery and building what matters',
    'Measuring to ensure updates are a success',
    'And much more!'
]

</script>

<style scoped>

</style>