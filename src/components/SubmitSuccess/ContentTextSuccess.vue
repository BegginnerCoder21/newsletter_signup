<template>
    <div class="md:space-y-4 space-y-8 mt-28 md:mt-0">
        <img src="../../assets/images/icon-success.svg" alt="" class="h-10 w-10">
        <h1 class="text-4xl font-bold">Thanks for subscribing!</h1>
        <p class="md:text-xs text-md  text-gray-500">A confirmation email has been sent to <span class="font-bold text-black">{{ props.email }} </span>  
            Please open it and click the button inside to confirm your subscription.</p>
            
        </div>
        <div class="mt-32 md:mt-0">
            <DismissMessageButton />
        </div>
</template>

<script setup lang="ts">
import DismissMessageButton from './DismissMessageButton.vue';

const props = defineProps<{
    email:string
}>();

</script>

<style scoped>

</style>