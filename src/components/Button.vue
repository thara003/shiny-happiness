<template>
    <button class="font-semibold py-1 px-3 mx-1 mt-2 rounded-md shadow-md"
        :class="[color === 'black' ? 'bg-black text-white' : 'bg-white border border-slate-300']">
        {{text}}
    </button>
</template>
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