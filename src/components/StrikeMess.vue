<template>
    <span>
        <strong class="font-semibold">Let's add it to the </strong>
        <span class="line-through font-semibold text-color decoration-2">main</span>
        <strong class="bg-violet-200 mx-1">secret</strong>
        <span>document</span>
        <span class="line-through font-semibold text-color decoration-2">ary</span>
        <strong class="bg-violet-200">s</strong>
    </span>
</template>
<style scoped>
.text-color {
  color: #b2ada9;
  text-decoration-skip: #b2ada9;
}
</style>
<script>
export default {
    name: 'StrikeMess',
}
</script>