<script setup lang='ts'>
</script>
<template>
   <div class="con">
      <div class="text">
         <h1> <slot name="title"></slot> </h1>
         <p> <slot name="summary"></slot> </p>
      </div>
      <div class="img"> 
         <slot name="img"></slot> 
      </div>
   </div>
</template>
<style lang="scss" scoped>
   .con{
      width: 320px;
      height: 280px;

      display: flex;
      flex-direction: column;
      justify-content: space-between;
      .text{
         h1{
            color: black;
            font-family: 'Work Sans', sans-serif;
            font-weight: 700;
            font-size: 2em;
            line-height: 110%;
            letter-spacing: 1.56px;
         }
         p{
            color: black;
            font-size: 1.25em;
            text-align: left;
         }
      }
   }
</style>
