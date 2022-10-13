<script>
import { defineComponent } from "vue";
import Notification from "./Notification.vue";

export default defineComponent({
  components: {
    Notification,
},
});
</script>

<template>
  <div class="flex items-center  justify-center">
  <Notification />
</div>
</template>

