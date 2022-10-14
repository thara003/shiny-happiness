<template>
    <button class="font-semibold py-1 px-3 mx-1 mt-2 rounded-md shadow"
        :class="[color === 'black' ? 'bg-black text-white' : 'bg-white border color']">
        {{text}}
    </button>
</template>
<style scoped>
.color {
    border-color: #dadada;
}
</style>
<script>
export default {
    name: 'Button',
    props: {
        text: {
            type: String,
            required: true,
        },
        color: {
            type: String,
            required: false,
        },
    },
}
</script>