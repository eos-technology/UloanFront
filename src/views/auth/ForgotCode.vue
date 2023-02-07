<template>
  <section class="signIn container">
    <img class="signIn__img" src="@/assets/img/Uloan.svg" alt="" />
    <div class="form signIn__form">
      <h2 class="title">Enter 4 Digits Code</h2>
      <p class="secondaryText">
        Enter the 4 digits number that you received on your email
        *****or@****.com
      </p>
      <div class="signIn__box">
        <input class="signIn__box-s" type="number" max="9" maxlength = "1"  />
        <input class="signIn__box-s" type="number" max="9" />
        <input class="signIn__box-s" type="number" max="9" />
        <input class="signIn__box-s" type="number" max="9" />
      </div>

      <a class="link signIn__link">Resend code</a>
    </div>
    <ButtonColor @click="$router.push({path:`resetPassword`})" class="signIn__btn" text="Send" />
  </section>
</template>

<script setup>
import ButtonColor from "@/components/form/ButtonColor.vue";
</script>

<style lang="scss" scoped>
.signIn {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 100vh;
  height: 100%;
  &__img {
    display: block;
    margin: 20% auto;
  }
  &__btn {
    margin-bottom: 20px;
  }
  &__form {
    margin-bottom: 100px;
    text-align: center;
  }
  &__link {
    text-decoration: underline;
  }
  &__box {
    display: flex;
    justify-content: space-evenly;
    &-s{
      padding: 12px 16px;
      border: 1px solid #eef0f1;
      border-radius: 4px;
      width: 53px;
      height: 48px;
      outline: none;
      -moz-appearance: textfield;
      &::-webkit-inner-spin-button,
      &::-webkit-outer-spin-button {
        -webkit-appearance: none;
        margin: 0;
      }
    }
  }
}
</style>