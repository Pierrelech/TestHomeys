<template>
  <main>
    <BoutonNotif @colorGenerated="handleColorGenerated" />
    <div class="notifications-container">
      <BaseNotification v-for="(notification, index) in notifications" :key="index" :color="notification.color" />
    </div>
  </main>
</template>

<script setup>
  import { ref } from 'vue';
  import BaseNotification from "./components/BaseNotification.vue";
  import BoutonNotif from "./components/BoutonNotif.vue";

  const notifications = ref([]);

  const handleColorGenerated = (color) => {
    notifications.value.push({ color });
  };
</script>

<style scoped>



.notifications-container {
  position: fixed;
  bottom: 0;
  left: 0;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 10px;
}

.notifications-container > * {
  margin-bottom: 10px;
}
</style>
