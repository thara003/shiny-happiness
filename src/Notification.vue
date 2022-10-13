<template>
      <div class = "m-20 lg:mt-80  box-border w-[28rem] rounded-2xl bg-white shadow-md">
    <div class="flex mx-4 m-2 pt-6 p-3">
        <h2 class="w-2/3 text-2xl font-extrabold ">Notifications</h2>
        <div class="w-1/3 flex justify-end items-centre">
            <a class="text-black font-semibold underline mt-1">Mark all as read</a>
        </div>
    </div>
    <a-tabs v-model:activeKey="activeKey" class="w-full text-black">
        <a-tab-pane key="1" class="bg-red"><template #tab>
                <span class="text-slate-500 pl-2" :class="[activeKey === '1' ? 'selected-tab' : '']">
                    All 
                </span>
                <span class="ml-1 text-s font-semibold rounded px-2 py-0.5" :class="[activeKey === '1' ? 'bg-black text-white' : 'bg-slate-200 text-slate-400']">8</span>
            </template>
            <Body />
        </a-tab-pane>
        <a-tab-pane key="2"><template #tab>
                <span class="text-slate-500" :class="[activeKey === '2' ? 'selected-tab' : '']">
                    Following
                </span>
                <span class="ml-1 text-s font-semibold rounded px-2 py-0.5" :class="[activeKey === '2' ? 'bg-black text-white' : 'bg-slate-200 text-slate-400']">6</span>
            </template>
            Content of Tab Pane 2
        </a-tab-pane>
        <a-tab-pane key="3"><template #tab>
                <span class="text-slate-500" :class="[activeKey === '3' ? 'selected-tab' : '']">
                    Archive
                </span>
            </template>
            Content of Tab Pane 3
        </a-tab-pane>
        <template #rightExtra>
            <setting-outlined :style="{fontSize: '20px', color:'rgb(148 163 184)', margin: '1rem', marginRight: '1.5rem'}" />
        </template>
    </a-tabs>
</div>
</template>
<style >
.ant-tabs-nav-wrap{
    margin-left: 1.5rem;
}
.ant-tabs-tab{
    padding-left: 0.5rem !important;
    padding-right: 0.5rem !important;
    margin-left: 0rem !important;
}
.ant-tabs-top > .ant-tabs-nav::before{
    border-bottom: 3px solid #f0f0f0 !important;
}

.ant-tabs-tab.ant-tabs-tab-active .ant-tabs-tab-btn {
    color: #363636 !important;
    font-weight: 700;
}

.ant-tabs-ink-bar {
    position: absolute;
    background: #000000 !important;
    pointer-events: none;
}

.selected-tab {
    color: #000000 !important;
    font-weight: 600;
}
</style>
<script lang="ts">
import { defineComponent, ref } from 'vue';
import { SettingOutlined } from '@ant-design/icons-vue';
import Body from './components/Body.vue';

export default defineComponent({
    components: {
    SettingOutlined,
    Body
},
    setup() {
        return {
            activeKey: ref('1'),
        };
    },
});
</script>
  