<template>
    <GoBack class="register__back"/>
  <section class="register container">
    <div class="form register__form">
      <h2 class="title">Recuperar contraseña</h2>
      <p class="secondaryText">Ingrese su dirección de correo electrónico a continuación y le enviaremos instrucciones para configurar una nueva</p>
      <BaseInput text="Email" type="email" placeholder="mail@example.com" />
    <ButtonColor @click="$router.push({path:`forgotCode`})" class="register__btn" text="Send" />
    </div>
  </section>
</template>

<script setup>
import ButtonColor from "@/components/form/ButtonColor.vue";
import BaseInput from "@/components/form/BaseInput.vue";
import GoBack from '@/components/base/GoBack.vue'
</script>

<style lang="scss" scoped>
.register {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 100vh;
  height: 100%;
  &__img {
    display: block;
    margin: 10% auto;
  }
  &__btn {
    margin-bottom: 20px;
  }
  &__form{
    padding-top: 50px;
    margin-bottom: 100px;
  }
  &__link{
    color: $color-btn-p;
  }
  &__back{
    margin-left: 24px;
    margin-top: 24px;
  }
}
</style>