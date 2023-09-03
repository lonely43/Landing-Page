<script setup lang='ts'>
import FAQquestionVue from './FAQquestion.vue';
</script>
<template>
   <main>
      <div class="textFAQ">
         <h1 class="titleText"> FAQ </h1>
      </div>
      <div class="questions">
         <FAQquestionVue>
            <template v-slot:title> How I can become you? </template>
            <template v-slot:answer> 
                  You just need 2 things: <br/>
                  &nbsp&nbsp 1 - pretty body <br/>
                  &nbsp&nbsp 2 - big brain </template>
         </FAQquestionVue>

         <FAQquestionVue>
            <template v-slot:title> Why? </template>
            <template v-slot:answer> Because </template>
         </FAQquestionVue>

         <FAQquestionVue>
            <template v-slot:title> 4 + 4? </template>
            <template v-slot:answer> 8 </template>
         </FAQquestionVue>

         <FAQquestionVue>
            <template v-slot:title> Пицца или суши? </template>
            <template v-slot:answer> Чай </template>
         </FAQquestionVue>
      </div>
   </main>
</template>
<style lang="scss" scoped>
   main{ 
      min-height: 100dvh;
      width: 100%;

      display: flex;
      justify-content: space-around;
      align-items: center;
   }
   .textFAQ{
      h1{
         font-weight: 600;
      } 
   }

   .questions{
      display: flex;
      flex-direction: column;
      gap: 2.68rem;
   }

   @media screen and (max-width: 800px) {
      main{
         flex-direction: column;
      }
   }
</style>
