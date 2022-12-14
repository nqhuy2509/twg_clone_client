<script setup lang="ts">

import { reactive } from 'vue';
import { UserOutlined, LockOutlined } from '@ant-design/icons-vue'

interface SignUp {
    email: string,
    phone_number: string,
    username: string,
    password: string
}

const signupState: SignUp = reactive<SignUp>({ email: '', phone_number: '', username: '', password: '' })

</script>

<template>

    <div class="containter">
        <a-form :model="signupState" name="normal_login" class="login-form">
            <h1>Đăng kí</h1>
            <a-form-item label="Email" name="email" :rules="[{ required: true, message: 'Vui lòng nhập email!' }]">
                <a-input v-model:value="signupState.email">
                    <template #prefix>
                        <UserOutlined class="site-form-item-icon" />
                    </template>

                </a-input>
            </a-form-item>

            <a-form-item label="Mật khẩu" name="password"
                :rules="[{ required: true, message: 'Vui lòng nhập mật khẩu' }]">
                <a-input-password v-model:value="signupState.password">
                    <template #prefix>
                        <LockOutlined class="site-form-item-icon" />
                    </template>
                </a-input-password>
            </a-form-item>

            <a-form-item label="Password" name="password"
                :rules="[{ required: true, message: 'Please input your password!' }]">
                <a-input-password v-model:value="signupState.password">
                    <template #prefix>
                        <LockOutlined class="site-form-item-icon" />
                    </template>
                </a-input-password>
            </a-form-item>

            <a-form-item>
                <a-button type="primary" html-type="submit" class="login-form-button">
                    Đăng kí
                </a-button>
                hoặc
                <a href="">Đăng nhập ngay!</a>
            </a-form-item>
        </a-form>

    </div>


</template>

<style scoped>
.containter {
    height: 100vh;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
}

.login-form {
    max-width: 300px;
}
</style>
