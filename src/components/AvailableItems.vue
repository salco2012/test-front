<template>
   <div class="available">
      <h3 class="available__title">
         Вещи на выбор
      </h3>
      <div v-for="item of allAvailableItems" :key="item.id" class="available__items">
         {{ item.name }}
      </div>
   </div>
</template>

<script>
   export default {
      data() {
         return {
            allAvailableItems: [
      {
         "id": 11,
         "name": "Jacket 1"
      },
      {
         "id": 12,
         "name": "Jacket 2"
      },
      {
         "id": 13,
         "name": "Jacket 3"
      },
      {
         "id": 14,
         "name": "Jacket 4"
      },
      {
         "id": 15,
         "name": "Hoodie 1"
      },
      {
         "id": 16,
         "name": "Hoodie 2"
      },
      {
         "id": 17,
         "name": "Hoodie 3"
      },
      {
         "id": 18,
         "name": "Hoodie 4"
      }
]
         }
      }
   }
</script>

<style lang="scss" scoped>
.available {
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
   &__items { 
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