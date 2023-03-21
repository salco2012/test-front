<template>
   <div>
      <div class="wrapper-selected-items">
         <selected-user-items />
         <selected-available-item />
      </div>
      <div class="wrapper-user-and-available">
         <user-items />
         <available-items />
      </div>
   </div>
</template>

<script>
import AvailableItems from './AvailableItems.vue';
import SelectedAvailableItem from './SelectedAvailableItem.vue';
import SelectedUserItems from './SelectedUserItems.vue';
import UserItems from './UserItems.vue';

export default {
   components: {
      AvailableItems,
      SelectedAvailableItem,
      SelectedUserItems,
      UserItems,
   },
   data() {
      return {
      
      }
   }
}
</script>

<style lang="scss" scoped>
.wrapper-selected-items, 
.wrapper-user-and-available {
   display: flex;
   align-items: center;
   justify-content: space-between;
   margin-bottom: 50px;
}

.wrapper-selected-items {
   margin-top: 50px;
}
</style>