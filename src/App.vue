<template>
  <main>
    <BoutonNotif @colorGenerated="handleColorGenerated" />
    <div class="notifications-container">
      <BaseNotification v-for="(notification, index) in notifications" :key="index" :color="notification.color" />
    </div>
  </main>
</template>

<script setup>
  import { ref, watch } from 'vue';
  import BaseNotification from "./components/BaseNotification.vue";
  import BoutonNotif from "./components/BoutonNotif.vue";

  const notifications = ref([]);

  const handleColorGenerated = (color) => {
    notifications.value.push({ color });
    console.log(color);
    console.log(notifications.value);

    // Vérification que la dernière valeur ajoutée correspond bien à la couleur générée
    const lastNotification = notifications.value[notifications.value.length - 1];
    if (lastNotification.color === color) {
        console.log('La couleur correspond bien:', color);
    } else {
        console.error('Erreur: La couleur ne correspond pas:', color, '!=', lastNotification.color);
    }
    if (notifications.value.length > 5) {
        notifications.value.shift();
        console.log('La plus ancienne notification a été supprimée');
    }
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
