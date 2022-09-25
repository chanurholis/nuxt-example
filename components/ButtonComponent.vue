<template>
    <button :class="styledButton">{{ name }}</button>
</template>

<script lang="ts">
export default {
    name: "ButtonComponent",
    data() {
        return {
            styledButton: "inline-flex justify-center whitespace-nowrap rounded-md border border-transparent bg-indigo-600 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700",
        }
    },
    props: {
        name: String,
        type: String,
    },
    methods: {
        typeButton() {
            const { type } = this.$props;

            switch (type) {
                case "primary":
                    this.styledButton = "inline-flex justify-center whitespace-nowrap rounded-md border border-transparent bg-blue-700 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700";
                    break;
                case "secondary":
                    this.styledButton = "inline-flex justify-center whitespace-nowrap rounded-md border border-transparent bg-gray-700 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700";
                    break;
                case "success":
                    this.styledButton = "inline-flex justify-center whitespace-nowrap rounded-md border border-transparent bg-green-700 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700";
                    break;
                case "info":
                    this.styledButton = "inline-flex justify-center whitespace-nowrap rounded-md border border-transparent bg-blue-400 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700";
                    break;
                case "warning":
                    this.styledButton = "inline-flex justify-center whitespace-nowrap rounded-md border border-transparent bg-yellow-700 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700";
                    break;
                case "danger":
                    this.styledButton = "inline-flex justify-center whitespace-nowrap rounded-md border border-transparent bg-red-700 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700";
                    break;
                default:
                    this.styledButton = "inline-flex justify-center whitespace-nowrap rounded-md border border-transparent bg-blue-700 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700";
                    break;
            }
        }
    },
    mounted() {
        this.typeButton();
    }
}
</script>