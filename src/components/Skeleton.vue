<template>
    <a-skeleton :paragraph="{ rows: 1 , width:130}" :title="{width: 250}" :avatar="{shape: 'square'}"/>
</template>
<style>
.ant-skeleton-header .ant-skeleton-avatar-lg.ant-skeleton-avatar-square {
    border-radius: 25% !important;
}
.ant-skeleton-content .ant-skeleton-title{
    height: 10px !important;
    margin-top: 5px !important;
}
.ant-skeleton-content .ant-skeleton-paragraph > li{
    height: 10px !important;
}
.ant-skeleton-content .ant-skeleton-title + .ant-skeleton-paragraph{
    margin-top: 4px !important;
}
</style>
<script>
export default {
    name: 'Skeleton',
}
</script>