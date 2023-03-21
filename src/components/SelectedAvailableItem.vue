<template>
   <div class="available">
         <div v-if="selectAvailable" class="available__item">
         {{ selectAvailable?.name }}
      </div>
   </div>
</template>

<script>
   export default {
      props: {
         selectAvailable: {
            type: Object,
            require: false,
            default: null,
         }
      }
   }
</script>

<style lang="scss" scoped>

.available {
   width: 25%;
   height: 25vh;
   border: 2px solid black;
   padding: 10px;
   position: relative;
   background: white;
   &__item {
      border: 2px solid green;
      width: 75px;
      height: 75px;
      display: flex;
      align-items: center;
      justify-content: center;
   }
}
</style>