<template>
    <div class="flex flex-col mt-7 md:mt-5 space-y-2">
        <label for="email" class="font-bold text-[10px] flex justify-between">Email address <span v-if="false" class=" text-orange-400">Valid email required </span></label>
        <input name="email" id="email" required type="text" class="h-10 w-full  placeholder:text-sm text-sm px-4 p-2 border border-gray-300 outline-2 hover:border outline-gray-400 hover:border-gray-400 rounded-md" placeholder="email@company.com ">
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped>

</style>