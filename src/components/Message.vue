<template>
  <div class="flex px-6 py-3">
    <div v-show="src" class="inline-flex w-10 h-11 relative">
      <img class='w-10 h-11 object-cover rounded-xl' alt='User avatar'
        :src="src">
      <span v-show="status"
      :class="[status === 'active' ? 'bg-green-500 ' : 'bg-red-500']"
        class="inline-flex w-3 h-3 absolute right-0 bottom-0 rounded-full ring-2 ring-white transform translate-x-1/3 translate-y-1/3"></span>
    </div>
    <div v-show="display === '2'" class=" bg-color inline-flex overflow-hidden relative justify-center items-center w-10 h-10 rounded-xl">
    <span class="font-medium text-black ">JR</span>
   </div>
   <div v-show="display === '5'" class="inline-flex overflow-hidden relative justify-center items-center w-10 h-10 bg-violet-200 rounded-xl ">
    <span class="font-medium text-black ">RT</span>
   </div>
    <div class="px-3">
      <span class="text-base"> <strong>{{strong1}} </strong>{{text}}<strong>{{strong2}}</strong></span>
      <span class="flex text-slate-500">{{timeago}}<li class="h-1 w-1 rounded-full bg-slate-400 mt-2 mx-1"
          v-show="listitem"></li>
        {{listitem}}</span>
      <Button text="Accept" color="black" v-if="button" />
      <Button text="Decline" v-if="button" />
      <div>
        <UploadMess v-if="upload" />
        <StrikeMess v-if="strike" />
      </div>
    </div>
  </div>
</template>
<style scoped>
.bg-color {
  background-color: #f2d1b0;
}
</style>
<script lang="ts">
import { UserOutlined } from '@ant-design/icons-vue';
import { defineComponent } from 'vue';
import Button from './Button.vue';
import UploadMess from './UploadMess.vue';
import StrikeMess from './StrikeMess.vue';
import { integer, number } from 'vue-types';
export default defineComponent({
  components: {
    UserOutlined,
    Button,
    UploadMess,
    StrikeMess
  },
  props: {
    display: {
      type: String,
      required: false
    },
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
    button: {
      type: Boolean,
      required: false,
    },
    upload: {
      type: Boolean,
      required: false,
    },
    strike: {
      type: Boolean,
      required: false,
    },
    src: {
      type: String,
      required: true,
    },
    status: {
      type: String,
      required: false,
    },
  },
});
</script>