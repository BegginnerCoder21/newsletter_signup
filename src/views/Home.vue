<template>
    <div v-if="false" class="md:w-[40rem] md:h-[27rem] w-[25rem] flex-col-reverse  bg-white md:rounded-3xl flex md:flex-row pb-3 md:p-4">
        <ContentText />
        <ContentImage />
    </div>
    <div v-else class="flex flex-col md:h-[19rem] h-full w-full md:w-[20rem] bg-white rounded-xl p-5">
        <ContentTextSuccess /> 
    </div>
</template>

<script setup lang="ts">
import  ContentText from '@/components/ContentText.vue';
import  ContentImage from '@/components/ContentImage.vue';
import  ContentTextSuccess from '@/components/SubmitSuccess/ContentTextSuccess.vue';

</script>x

<style scoped>

</style>