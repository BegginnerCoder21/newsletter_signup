<template>
    <div v-if="validValues" class="md:w-[40rem] md:h-[27rem] w-[25rem] flex-col-reverse  bg-white md:rounded-3xl flex md:flex-row pb-3 md:p-4">
        <div class="mt-10 px-5 md:px-7">
            <h1 class="text-4xl font-bold">Stay updated!</h1>
            <p class="md:text-sm text-md text-gray-400 mt-4 md:mt-3">Join 60,000+ product managers receiving monthly updates on:</p>
            <ProductList />
            <Email @submit-button="ValidValue" />
        </div>
        <ContentImage />
    </div>
    <div v-else class="flex flex-col md:h-[19rem] h-full w-full md:w-[20rem] bg-white rounded-xl p-5">
        <ContentTextSuccess :email="emails" /> 
    </div>
</template>

<script setup lang="ts">
import  ContentImage from '@/components/ContentImage.vue';
import ProductList from '../components/ProductList.vue';
import Email from '../components/Email.vue';
import  ContentTextSuccess from '@/components/SubmitSuccess/ContentTextSuccess.vue';
import { ref } from 'vue';
const emails = ref<string>('');

const validValues = ref<boolean>(true);

const ValidValue = (email:string) => {
    validValues.value = false;
    emails.value = email;
}

</script>

<style scoped>

</style>