<template>
  <div class="flex ">
    <a-avatar shape="square" size="large" class="rounded-lg">
      <template #icon>
        <UserOutlined />
      </template>
    </a-avatar>
    <div class="px-3">
      <span class="text-base"> <strong>{{strong1}} </strong>{{text}}<strong>{{strong2}}</strong></span>
      <span class="flex text-slate-500">{{timeago}}<li class="h-1 w-1 rounded-full bg-slate-400 mt-2 mx-1" v-if="listitem"></li>
        {{listitem}}</span>
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
  props: {
    strong1: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
    strong2: {
      type: String,
      required: false,
    },
    timeago: {
      type: String,
      required: true,
    },
    listitem: {
      type: String,
      required: false,
    },
  },
});
</script>