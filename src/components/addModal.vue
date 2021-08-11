<template>
  <div class="add-modal">
    <form action="">
      <label class="heading_sm add-modal__label" for="fullName">
        <span>Full Name:</span>
        <input class="add-modal__input" type="text" name="fullName" id="fullName">
      </label>
      <label for="email" class="heading_sm add-modal__label-email">
        <span>Email:</span>
        <input type="email" name="email" id="email" class="add-modal__input">
      </label>
      <label for="data" class="heading_sm add-modal__label-data">
        <span>Data:</span>
        <input type="date" name="data" id="data" class="add-modal__input">
      </label>
      <label for="time" class="heading_sm add-modal__label-time">
        <span>Visit Time:</span>
        <input type="time" name="time" id="time" class="add-modal__input">
      </label>
      <label for="doctor" class="heading_sm add-modal__label-doctor">
        <span>Doctor:</span>
        <input type="text" name="doctor" id="doctor" class="add-modal__input">
      </label>
      <label for="conditions" class="heading_sm add-modal__label-conditions">
        <span>Conditions:</span>
        <input type="text" name="conditions" id="conditions" class="add-modal__input">
      </label>
      <button type="submit" class="btn-change" @click="openModal()">Change</button>
    </form>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss">
  .add-modal {
    position: absolute;
    padding: 40px;
    background: #FFFFFF;
    box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
    border-radius: 8px;
    z-index: 1000px;
    &__label {
      display: flex;
      gap: 10px;
      align-items: center;
      padding: 10px 0;
    }
    &__input {
      outline: none;
      padding: 5px 20px 5px 10px;
      border: 1px solid black
    }
    &__label-email {
      display: flex;
      align-items: center;
      gap: 39px;
      padding: 10px 0;
    }
    &__label-data {
      display: flex;
      align-items: center;
      gap: 43px;
      padding: 10px 0;
    }
    &__label-time {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 10px 0;
    }
    &__label-doctor {
      display: flex;
      align-items: center;
      gap: 28px;
      padding: 10px 0;
    }
    &__label-conditions {
      display: flex;
      align-items: center;
      gap: 5px;
      padding: 10px 0;
    }
    .btn-change {
      padding: 10px 40px;
      border: none;
      outline: none;
      border-radius: 12px;
      color: #333;
      background-color: beige;
      cursor: pointer;
      margin-left: 50%;
      transform: translate(-50%);
      margin-top: 20px;
      &:hover {
        background-color: rgb(206, 206, 203);
      }
    }
  }
</style>