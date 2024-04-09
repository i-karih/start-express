<script setup>
import Modal from '../UI/modals/modal.vue'
import Input from '../UI/form/input.vue'
import Button from '../UI/buttons/button.vue'

</script>

<template>
    <Modal
      title="Вход"
      size="small"
      classModal="auth-modal"
    >
        <template #body>
            <div class="auth-modal__inputs">
                <Input placeholder="Введите почту"/>
                <Input placeholder="Введите пароль"/>
                <div class="auth-modal__buttons">
                    <Button label="Войти"/>
                    <Button type="outline-orange" label="Регистрация"/>
                </div>
            </div>
        </template>
    </Modal>
</template>

<style lang="scss">
    .auth-modal {
        &__inputs {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        &__buttons {
            display: flex;
            gap: 10px;
            & .default-btn {
                width: calc(50% - 5px);
            }
        }
    }
</style>