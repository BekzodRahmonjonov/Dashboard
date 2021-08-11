<template>
  <div class="home">
    <Aside />
    <Container />
  </div>
</template>

<script>
import Aside from '../components/Aside.vue'
import Container from '../components/Container.vue'

export default {
  name: 'Home',
  components: {
    Aside,
    Container
  }
}
</script>

<style lang="scss">
  // Fonts import
  @import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap');
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  .link {
    text-decoration: none;
  }
  .list {
    list-style-type: none;
  }
  .heading_xl {
    font-family: "Lato";
    font-weight: bold;
    font-size: 40px;
    line-height: 46px;
    letter-spacing: 0.2px;
    color: #25282B;
  }
  .heading {
    font-family: "Lato";
    font-weight: bold;
    font-size: 20px;
    line-height: 26px;
    letter-spacing: 0.2px;
    color: #25282B;
  }
  .heading_sm, .paragraph {
    font-family: "Lato";
    font-weight: bold;
    font-size: 14px;
    line-height: 20px;
    letter-spacing: 0.1px;
    color: #52575C;
  }
  .paragraph {
    font-weight: normal;
  }
  .heaing_grey {
    font-family: "Lato";
    font-weight: bold;
    font-size: 10px;
    line-height: 12px;
    letter-spacing: 0.2px;
    color: #A0A4A8;
  }
  .heading_sm_normal {
    font-family: "Lato";
    font-size: 14px;
    line-height: 20px;
    letter-spacing: 0.1px;
    color: #52575C;
  }
  // Home page styles
  .home {
    display: flex;
  }
  @media screen and (max-width: 1300px) {
    .intro-card {
      width: 220px;
    }
  }
  @media screen and (max-width: 1200px) {
    .intro-card {
      width: 200px;
      padding: 10px 18px;
    }
    .body-conditions, .appointment-table__conditions {
      display: none;
    }
    .appointment-table__email {
      flex-basis: 25%;
    }
    .body-email {
      flex-basis: 25% !important;
    }
    .appointment-table__date {
      flex-basis: 13%;
    }
    .appointment-table__body-item .body-date {
      flex-basis: 13%;
    }
    .body-doctor {
      flex-basis: 19% !important;
    }
  }
  @media screen and (max-width: 1100px) {
    .intro-card {
      width: 180px;
    }
    .appointment-table__visit, .body-time {
      display: none;
    }
    .appointment-table__email {
      flex-basis: 30%;
    }
    .body-email {
      flex-basis: 30% !important;
    }
    .appointment-table__date {
      flex-basis: 15%;
    }
    .body-date {
      flex-basis: 15% !important;
    }
    .appointment-table__doctor {
      flex-basis: 17%;
    }
    .body-doctor {
      flex-basis: 24% !important;
    }
  }
  @media screen and (max-width: 1000px) {
    .container {
      height: 130vw;
    }
    .intro {
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      &-card {
        width: 220px;
        padding: 14px 20px;
      }
    }
    .appointment-table__doctor, .body-doctor {
      display: none;
    }
    .appointment-table__email {
      flex-basis: 40%;
    }
    .body-email {
      flex-basis: 40% !important;
    }
    .body-date {
      flex-basis: 22% !important;
    }
  }
  @media screen and (max-width: 900px) {
    .container {
      height: 147vw;
    }
  }
  @media screen and (max-width: 800px) {
    .aside {
      width: 70px;
    }
    .container {
      margin-left: 70px;
      flex-basis: 91%;
      height: 162vw;
    }
    .aside-list {
      .heading_sm {
        display: none;
      }
    }
    .aside__last-heading {
      display: none;
    }
    .logo {
      width: 33px;
      overflow: hidden;
      transform: translate(-6px);
    }
  }
  .chart {
    width: 600px;
    margin: 0 auto;
    margin-top: 30px;
  }
  @media screen and (max-width: 700px) {
    .avatar-name, .appointment-table__name {
      flex-basis: 33% !important;
    }
    .chart {
      width: 100%;
    }
  }
  @media screen and (max-width: 600px) {
    .container {
      height: 250vw;
    }
    .avatar-name, .appointment-table__name {
      flex-basis: 18% !important;
    }
    .avatar-name {
      .paragraph {
        display: none;
      }
    }
    .body-email, .appointment-table__email {
      flex-basis: 50% !important;
    }
  }
  @media screen and (max-width: 550px) {
    .header__input-item {
      width: 200px;
    }
    .body-date, .appointment-table__date {
      display: none;
    }
    .body-email, .appointment-table__email {
      flex-basis: 66% !important;
    }
    .add-icon {
      margin-left: 2% !important;
    }
    .container {
      height: 268vw;
    }
  }
  @media screen and (max-width: 500px) {
    .container {
      height: 310vw;
    }
  }
  @media screen and (max-width: 450px) {
    .container {
      height: 330vw;
    }
    .appointment-table__body-item .body-email {
      display: none;
    }
    .avatar-name {
      flex-basis: 85% !important;
      .paragraph {
        display: block;
      }
    }
    .appointment-table__email {
      display: none
    }
    .avatar-name, .appointment-table__name {
      flex-basis: 88% !important;
    }
  }
  @media screen and (max-width: 450px) {
    .container {
      height: 370vw;
    }
  }
</style>
