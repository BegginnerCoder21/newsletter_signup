<template>
    <div class="flex flex-col mt-7 md:mt-5 space-y-3">
        <label for="email" class="font-bold text-[10px] flex justify-between">Email address <span v-if="errorValue" class=" text-orange-400">Valid email required </span></label>
        <input v-model="inputEmail" name="email" id="email" required type="text" :class="{'border-2 border-red-400 bg-red-300':errorValue } " class="h-10 w-full  placeholder:text-sm text-sm px-4 p-2 border border-gray-300 outline-2 hover:border outline-gray-400 hover:border-gray-400 rounded-md" placeholder="email@company.com ">
        <SubmitButton @submit-form="SubmitForm" />
    </div>
</template>

<script setup lang="ts">

import {ref } from 'vue';
import SubmitButton from './SubmitButton.vue';
const inputEmail = ref<string>('');
const errorValue = ref<boolean>(false);
const emit = defineEmits<{
    (e:'submit-button'):void
}>();

const SubmitForm = () => {
    let res = /^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$/;
    let validEmail = res.test(inputEmail.value);
    
    if(!inputEmail.value || !validEmail){
        errorValue.value = true;
        setTimeout(() => {
            errorValue.value = false;
        } , 2000)
    }else{
        emit('submit-button');
    }
}

</script>

<style scoped>

</style>