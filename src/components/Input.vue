<template>
    <div>
        <input type="text" v-model="text" @keyup.enter="submit">
        <button @click="submit">新增</button>
    </div>
</template>

<script>
export default {
    name: "Input",
    data: () => {
        return {
            text: ""
        }
    },
    methods: {
        submit() {
            this.$emit("input_text", this.text);
            this.text = "";
        }
    }
}
</script>
