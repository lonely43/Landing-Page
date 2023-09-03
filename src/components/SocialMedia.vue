<script setup lang='ts'>

</script>
<template>
   <main>
      <div class="socialMedia">
         <a href=""><img src="../assets/socialMedia/telegram.png" alt="tg"></a>
         <a href=""><img src="../assets/socialMedia/discord.png" alt="discord"></a>
         <a href=""><img src="../assets/socialMedia/github.png" alt="gitHub"></a>
      </div>
   </main>
</template>
<style lang="scss" scoped>
   main{
      min-height: 100dvh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      .socialMedia{
         padding: 1rem 2rem;

         display: flex;
         flex-direction: row;
         gap: 2rem;

         border-radius: 0rem;
         border-top: 0.2rem solid rgb(0, 0, 0);
         border-bottom: 0.2rem solid rgb(0, 0, 0);

         a{
            width: 46px;
            height: 46px; 
         }
         img{
            width: 100%;
            height: 100%; 
         }
      }
   }
</style>
