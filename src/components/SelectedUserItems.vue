<template>
   <div class="user">
      <h3 class="user__title" title="Из вещей пользователя">
         Выбранные вещи
      </h3>
   </div>
</template>

<script>
   export default {
      
   }
</script>

<style lang="scss" scoped>
.user {
   width: 25%;
   height: 20vh;
   border: 2px solid black;
   padding: 10px;
   position: relative;
   background: white;
   &__title {
      position: absolute;
      top: -50px;
      left: 50%;
      transform: translate(-50%, 0);
      font-size: 18px;
      background: orange;
      color: rgb(120, 78, 0);
      padding: 5px 10px;
      border-radius: 5px 5px 0 0;
      z-index: -1;
      cursor: help;
   }
}
</style>