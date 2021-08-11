<template>
  <div class="appointment-table__body-item" :class="isActive ? 'd-none' : ''">
    <span class="avatar-name">
      <img :src="avatarImg" alt="Avatar Image">
      <span class="paragraph full-name"> {{ fullName }} </span>
    </span>
    <span class="body-email paragraph"> {{ email }} </span>
    <span class="body-date paragraph"> {{ date }} </span>
    <span class="body-time paragraph"> {{ visitTime }} </span>
    <span class="body-doctor paragraph"> {{ doctor }} </span>
    <span class="body-conditions paragraph"> {{ conditions }} </span>
    <span class="body-icons">
      <span class="body-edit" v-html="editIcon" @click="openModal()"></span>
      <span class="body-delete" v-html="deleteIcon" @click="deleteFunc()"></span>
    </span>
    <div class="modalBg" @click="openModal()" :class="modalActive ? 'd-inline-block' : ''">
      <addModal @click="modalActive" />
    </div>
  </div>
</template>

<script>
import addModal from './addModal.vue'

export default {
  components: {
    addModal
  },
  props: [
    'avatarImg',
    'fullName',
    'email',
    'date',
    'visitTime',
    'doctor',
    'conditions',
    'editIcon',
    'deleteIcon'
  ],
  data () {
    return {
      isActive: false,
      modalActive: false
    }
  },
  methods: {
    deleteFunc: function () {
      this.isActive = !this.isActive
    },
    openModal: function () {
      this.modalActive = !this.modalActive
    }
  },
  // watch: {
  //   openModal () {
  //     if(this.openModal) {
  //       document.querySelector('.home')
  //       console.log('salomchik')
  //     }
  //   }
  // }
}
</script>

<style lang="scss">
  .appointment-table__body-item {
    padding: 14px 24px;
    display: flex;
    align-items: center;
    .modalBg {
      width: 100vw;
      height: 100vh;
      position: absolute;
      top: 0;
      left: 0;
      background: #0000002c;
      display: none;
    }
    .avatar-name {
      display: flex;
      align-items: center;
      gap: 12px;
      flex-basis: 23%;
    }
    .body-email {
      flex-basis: 23%;
    }
    .body-date {
      flex-basis: 10%;
    }
    .body-time {
      flex-basis: 15%;
    }
    .body-doctor, .body-conditions {
      flex-basis: 12%;
    }
    .body-icons {
      display: flex;
      gap: 10px;
      .body-delete {
        cursor: pointer;
      }
      .body-edit {
        cursor: pointer;
      }
    }
  }
  .d-none {
    display: none !important;
  }
  .d-inline-block {
    display: inline-block !important;
    position: fixed !important;
    top: 0 !important;
    left: 0 !important;
  }
</style>