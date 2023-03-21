<template>
   <div class="user">
      <div v-for="(item, index) in selectUserItems" :key="index" class="user__item">
         {{ item.name }}
      </div>
   </div>
</template>

<script>
   export default {
      props: {
         selectUserItems: {
            type: Array,
            require: false,
         }
      }
   }
</script>

<style lang="scss" scoped>
.user {
   width: 25%;
   height: 25vh;
   border: 2px solid black;
   padding: 10px;
   position: relative;
   background: white;
   display: flex;
   align-content: flex-start;
   flex-wrap: wrap;
   &__item {
      border: 2px solid green;
      width: 75px;
      height: 75px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 5px;
      margin-bottom: 5px;
   }
}
</style>