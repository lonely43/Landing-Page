<script setup lang='ts'>

</script>
<template>
   <div class="picture">
      <div loading="eager" class="img"></div>
   </div>
</template>
<style lang="scss" scoped>
   .picture{

      overflow-x: hidden;
      .img{
         min-height: 100dvh;
         height: 100vh;

         display: flex;
         justify-content: center;
         align-items: center;
         text-align: center;

         background-image: linear-gradient(to bottom, rgba(7, 7, 7, 0.219) 0%, rgba(99, 37, 90, 0) 60%, var(--color-background) 100%), url(../assets/enigma.jpg);
         background-position: center;
         background-repeat: no-repeat;
         background-size: cover;


         overflow-x: hidden;
      }
   }
</style>
