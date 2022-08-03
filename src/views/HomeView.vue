<script setup>
import Message from '@/components/Message.vue'
import TheList from '../components/TheList.vue';
</script>

<template>
  <main>
    <div class="container flex flex-col center mx-auto w-12/12 lg:w-12/12 snap-y snap-mandatory w-12/12 h-screen overflow-scroll">
    <Message />
    <TheList />
    </div>
  </main>
</template>
