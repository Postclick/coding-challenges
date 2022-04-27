<template>
    <div
        class="node"
        v-bind:style="{top: y + 'px', left: x + 'px', background: selected ? 'black' : 'radial-gradient(circle at 24px 24px, #fff -70%, ' + color + ' 70%)'}"
    ></div>
</template>

<script>
export default {
    name: 'CircleNode',
    components: {},
    props: {
        id: {type: Number},
        x: {type: Number},
        y: {type: Number},
        color: {type: String},
        selected: {type: Boolean}
    },
}
</script>

<style>
    .node {
        position: absolute;
        background-color: white;
        height: 64px;
        width: 64px;
        border-radius: 50%;
        box-shadow: 2px 2px 10px -1px rgb(59, 59, 59);
    }
</style>
