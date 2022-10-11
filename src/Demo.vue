<template>
    <div class="flex m-2">
        <h2 class="w-2/3 text-2xl font-extrabold ">Notifications</h2>
        <div class="w-1/3 flex justify-end items-centre">
            <a class="text-black font-semibold underline">Mark all as read</a>

        </div>
    </div>
    <a-tabs v-model:activeKey="activeKey" class="w-full text-black">
        <a-tab-pane key="1"><template #tab>
                <span class="text-slate-500 text-s" :class="[activeKey === '1' ? 'selected-tab' : '']">
                    All 
                </span>
                <span class="ml-1 text-s font-semibold rounded px-2 py-0.5" :class="[activeKey === '1' ? 'bg-black text-white' : 'bg-slate-200 text-slate-400']">8</span>
            </template>
            Content of Tab Pane 1
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
            <setting-outlined :style="{fontSize: '20px'}" />
        </template>
    </a-tabs>
</template>
<style >
.ant-tabs-tab.ant-tabs-tab-active .ant-tabs-tab-btn {
    color: #363636 !important;
    font-weight: 700;
}

/* :hover {
    color: #363636 !important;
} */

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

export default defineComponent({
    components: {
        SettingOutlined,
    },
    setup() {
        return {
            activeKey: ref('1'),
        };
    },
});
</script>
  