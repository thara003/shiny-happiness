<script>
import { defineComponent } from "vue";
import Demo from "./Demo.vue";

export default defineComponent({
  components: {
    Demo,
  },
});
</script>

<template>
  <div class = "justify-center items-center box-border w-[32rem] p-4 rounded-lg bg-white shadow-md">
  <demo />
</div>
</template>

