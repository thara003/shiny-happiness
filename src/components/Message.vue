<template>
    <div class="flex m-2">
    <a-avatar shape="square" size="large" class="rounded-lg">
    <template #icon><UserOutlined /></template>
  </a-avatar>
    <div class="px-3">
        <span class="text-base"> <strong>Anna Srzand </strong>joined to 🔥 <strong>Final Presentation</strong></span>
        <span class="flex text-slate-500">2h ago<li class="h-1 w-1 rounded-full bg-slate-400 mt-2 mx-1"></li>Socila Media Plan</span>
    </div>
    </div>
</template>
<script lang="ts">
import { UserOutlined } from '@ant-design/icons-vue';
import { defineComponent } from 'vue';
export default defineComponent({
  components: {
    UserOutlined,
  },
});
</script>