<script setup lang='ts'>
import { ref } from 'vue';
   defineProps<{
      title?: string,
      answer?: string
}>()

const block = ref()
const arrow = ref()

const isActive = ref<boolean>(false)

function hadle(){
   if(isActive.value){
      block.value.classList.remove('show')
      arrow.value.style.transform = `rotate(0deg)`;
   }
   else{
      block.value.classList.add('show')
      arrow.value.style.transform = `rotate(180deg)`;
   }
   isActive.value = !isActive.value
}
</script>
<template>
   <div ref="block" class="block">
      <div class="text">
         <h1 @click="hadle"> <slot name="title"></slot></h1>
         <svg ref="arrow" xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chevron-down" viewBox="0 0 16 16"><path fill-rule="evenodd" d="M1.646 4.646a.5.5 0 0 1 .708 0L8 10.293l5.646-5.647a.5.5 0 0 1 .708.708l-6 6a.5.5 0 0 1-.708 0l-6-6a.5.5 0 0 1 0-.708z"/></svg>
      </div>
      <p> <slot name="answer"></slot> </p>
   </div>   
</template>
<style lang="scss" scoped>
   .block{

      .text{
         display: flex;
         justify-content: space-between;
         gap: 2rem;
      }
      width: 100%;
      height: auto;

      display: grid;
      grid-template-rows: 1rem 0fr;
      gap: 1.25rem;

      padding-bottom: 0.2rem;
      border-bottom: 0.1rem solid rgba(25, 25, 25, 0.05);

      transition: grid-template-rows 200ms; 

      h1{
         position: relative;

         cursor: pointer;

         line-height: 110%;
         font-weight: 600;
         font-size: 1.68em;
         text-transform: none;
         letter-spacing: 1px;

         display: flex;
         align-items: center;

         svg{
            transition: 200ms;
         }
      }
      p{
         font-size: 1.25em;
         text-align: left;

         overflow: hidden;
      }
   }
   .show{
      grid-template-rows: 1rem 1fr;
   }
</style>
