<template>
    <div>
        <Input @input_text="PushTo"></Input>
        <ul>
            <Item v-for="(item, id) in list" :key="id" :item="item" :index="id" @del_item="del"></Item>
        </ul>
    </div>
</template>

<script>
import Input from "../components/Input.vue";
import Item from "../components/Item.vue";
export default {
    name: "Index",
    components: {
        Input,
        Item
    },
    data: () => {
        return {
            list: []
        }
    },
    methods: {
        PushTo(val) {
            this.list.push(val);
        },
        del(id) {
            this.list.splice(id, 1);
        }
    }
}
</script>

