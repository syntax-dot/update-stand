<template>
  <router-view/>
</template>

<script setup lang="ts">

import { addPushNotificationsListeners, registerNotifications } from 'src/utils/push-notifications'
import { onMounted } from 'vue'

onMounted(async () => {
  await addPushNotificationsListeners()
  await registerNotifications()
})

</script>
