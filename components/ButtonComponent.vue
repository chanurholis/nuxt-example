<template>
    <button :class="styledButton">{{ name }}</button>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
    name: "ButtonComponent",
    props: {
        name: {
            type: String,
            required: true
        },
        type: {
            type: String,
        },
    },
    data() {
        return {
            styledButton: "inline-flex justify-center whitespace-nowrap rounded-md border border-transparent px-4 py-2 text-base font-medium text-white shadow-sm",
        }
    },
    created() {
        const { type } = this.$props;

        switch (type) {
            case "primary":
                this.styledButton += " bg-blue-700 hover:bg-blue-400";
                break;
            case "secondary":
                this.styledButton += " bg-gray-700 hover:bg-gray-400";
                break;
            case "success":
                this.styledButton += " bg-green-700 hover:bg-green-400";
                break;
            case "info":
                this.styledButton += " bg-blue-400 hover:bg-blue-200";
                break;
            case "warning":
                this.styledButton += " bg-yellow-700 hover:bg-yellow-400";
                break;
            case "danger":
                this.styledButton += " bg-red-700 hover:bg-red-400";
                break;
            default:
                this.styledButton += " bg-pink-700 text-black hover:bg-pink-400";
                break;
        }
    }
})
</script>