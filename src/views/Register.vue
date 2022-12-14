<script setup lang="ts">

import { reactive } from 'vue';
import { Button } from 'ant-design-vue'
const ButtonGroup = Button.Group

interface SignUp {
    email: string,
    phone_number: string,
    username: string,
    password: string
}

const state: SignUp = reactive({ email: '', phone_number: '', username: '', password: '' })

</script>

<template>

    <a-button type="primary">Primary Button</a-button>
</template>
