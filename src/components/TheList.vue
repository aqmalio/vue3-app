<script setup>
import Item from './Item.vue'
import { useCaringStore } from '../stores/caring';
import IconDocumentationVue from './icons/IconDocumentation.vue';


const carings = useCaringStore();

</script>

<template>
<div class="mt-6">
  <ul role="list" class="">
    <li v-for="(data, index) in carings.data" class="snap-start w-screen h-screen" style="scroll-snap-align: start;">
      <Item :index="index">
        <template #heading>
          <div class="flex items-center">
            <div class="ring-emerald-400 p-2 bg-emerald-500 block text-white drop-shadow shadow-slate-600 rounded-sm"><IconDocumentationVue /></div>
            <h5 class="text-xl px-2">{{data.title}}</h5>
          </div>
        </template>
        <ul v-for="(list, l) in data.list" class="list-none border-b-2  ">
          <li class="text-zinc-700 my-2 ml-5">{{list}}</li>
        </ul>
      </Item>
    </li>
    </ul>
  </div>
  <!-- <div class="mt-6">
    <a href="#" class="w-full flex justify-center items-center px-4 py-2 border border-gray-300 shadow-sm text-sm font-medium rounded-md text-gray-700 bg-white hover:bg-gray-50"> View all </a>
  </div> -->
  

</template>
