<template>
  <div class="footer">
    <img
      src="../assets/images/logo.png"
      alt="company logo"
      class="footer__logo"
    >
    <span>*Terms and Conditions Apply</span>
  </div>
</template>

<script>
  export default {

  }
</script>

<style lang="scss" scoped>
  .footer {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;

    position: absolute;
    bottom: 0;
    width: 100vw;
    padding: 70px;

    font-family: Arial;
    font-size: 14px;
    color: #464646;

    z-index: 5;

    @media (max-width: 1200px) {
      bottom: inherit;
      top: 0;
      align-items: center;
    }

    @media (max-width: 768px) {
      font-size: 10px;
    }

    @media (max-width: 480px) {
      padding: 20px;
    }

    &__logo {
      @media (max-width: 768px) {
        height: 25px;
        margin-right: 50px;
      }
    }
  }
</style>
