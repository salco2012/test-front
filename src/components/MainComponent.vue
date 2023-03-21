<template>
   <div>
      <div class="wrapper-selected-items">
         <selected-user-items :selectUserItems="userItems"/>
         <selected-available-item :selectAvailable="selectAvailableItem"/>
      </div>
      <div class="wrapper-user-and-available">
         <user-items @select-user-click="selectUser"/>
         <available-items @select-available="selectAvailable"/>
      </div>
      <div style="display: flex; justify-content: center; margin-bottom: 20px;">
         <button class="btn" @click="setStorage">Сохранить выбранные вещи в Local Storage</button>
         <button class="btn" @click="clearStorage">Очистить Local Storage</button>
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
         selectAvailableItem: null,
         userItems: [],
      }
   },
   created() {
      if (localStorage.getItem('selectAvailableItem')) {
      this.selectAvailableItem = JSON.parse(localStorage.getItem('selectAvailableItem'));
      }
      if (localStorage.getItem('userItems')) {
      this.userItems = JSON.parse(localStorage.getItem('userItems'));
      }
   },
   methods: {
      selectAvailable(item) {
         this.selectAvailableItem = item;
      },
      selectUser(item) {
         if (this.userItems.length < 6 && !this.userItems.some(obj => obj.id === item.id)) {
            this.userItems.push(item);
            
         }
      },
      setStorage() {
         localStorage.setItem('selectAvailableItem', JSON.stringify(this.selectAvailableItem));
         localStorage.setItem('userItems', JSON.stringify(this.userItems));
         alert('Данные сохранены')
      },
      clearStorage() {
         localStorage.clear();
         window.location.reload();
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

.btn {
   cursor: pointer;
   border: none;
   padding: 10px 15px;
   font-size: 16px;
   margin-right: 20px;
   margin-top: -30px;
   background: orange;
   color: rgb(120, 78, 0);
}
</style>