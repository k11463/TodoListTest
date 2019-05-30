<template>
    <li @click="del(index)" class="li">
        {{item}}
    </li>
</template>

<script>
export default {
    name: "Item",
    props: [
        "item", "index"
    ],
    methods: {
        del(id) {
            this.$emit("del_item", id);
        }
    }
}
</script>

<style lang="scss" scoped>
.li{
    cursor: pointer;
}
</style>

