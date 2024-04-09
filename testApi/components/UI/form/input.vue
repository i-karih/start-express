<script setup>
const props = defineProps({
    type: {
        type: String,
        default: "text",
    }, 
    placeholder: {
        type: String,
        default: "Введите значение",
    }
})
const inputValue = ref("")
</script>

<template>
    <div class="default-input">
        <input v-model="inputValue" :type="type" :placeholder="placeholder">
    </div>
</template>

<style lang="scss">
    .default-input {
        & input {
            width: 100%;
            padding: 15px 20px;
            font-size: 14px;
            font-weight: 300;
            border: 1px solid #c1c1c1;
            border-radius: 10px;
            color: #3c3a3a;
            transition: border 0.3s;
            &:focus {
                border: 1px solid #7b8ee2;
            }
        }
    }
</style>