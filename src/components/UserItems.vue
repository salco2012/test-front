<template>
   <div class="user">
      <h3 class="user__title">Вещи у пользователя</h3>
      <div class="user__item" v-for="item in allItems" :key="item.id">
            {{ item.name }}
      </div>
   </div>
</template>

<script>
   export default {
      data() {
         return {
         allItems: [
      {
         "id": 1,
         "name": "Shoes 1"
      },
      {
         "id": 2,
         "name": "Shoes 2"
      },
      {
         "id": 3,
         "name": "Shoes 3"
      },
      {
         "id": 4,
         "name": "Shoes 4"
      },
      {
         "id": 5,
         "name": "T-shirt 1"
      },
      {
         "id": 6,
         "name": "T-shirt 2"
      },
      {
         "id": 7,
         "name": "T-shirt 3"
      },
      {
         "id": 8,
         "name": "T-shirt 4"
      }
],
         }
      }
   }
</script>

<style lang="scss" scoped>
.user {
   width: calc(50% - 30px);
   height: 50vh;
   border: 2px solid black;
   padding: 10px;
   display: flex;
   flex-wrap: wrap;
   align-content: flex-start;
   gap: 10px;
   position: relative;
   background: white;
   &__item { 
      width: 100px;
      height: 100px;
      border: 2px solid black;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all .4s ease;
      &:hover {
         border: 2px solid orange;
         cursor: pointer;
      }
   }
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
   }
}
</style>