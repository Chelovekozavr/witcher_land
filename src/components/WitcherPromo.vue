<template>
  <div class="promo">
    <h2 class="promo__text-title">300%</h2>
    <h3 class="promo__text">Welcome bonus</h3>

    <div class="promo__code-container">
      <h1 class="promo__code">{{code}}</h1>
      <span class="promo__copy-code" v-clipboard:copy="code">Copy code</span>
    </div>

    <button class="promo__button">Play now</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        code: 'WITCHER'
      }
    }
  }
</script>

<style lang="scss" scoped>
  .promo {
    display: flex;
    flex-direction: column;
    align-items: center;

    position: absolute;
    top: 205px;
    right: 240px;

    font-family: Cambria;
    text-transform: uppercase;

    z-index: 4;

    @media (max-width: 1600px) {
      right:70px;
    }

    @media (max-width: 1380px) {
      right:70px;
      transform: scale(0.8);
    }

    @media (max-width: 1200px) {
      justify-content: center;
      top: 100px;
      right: 0;

      height: 100%;
      width: 100%;

      transform: scale(0.9);
    }

    @media (max-width: 969px) {
      top: 200px;
    }

    @media (max-width: 480px) {
      top: 100px;
      transform: scale(0.6);
    }

    @media (max-width: 320px) {
      top: 50px;
    }

    &__text-title {
      font-size: 208.55px;
      line-height: 286.75px;
      color: #fff;

      @media (max-width: 600px) {
        font-size: 180px;
      }

      @media (max-width: 480px) {
        font-size: 140px;
      }
    }

    &__text {
      font-size: 67.58px;
      line-height: 92.92px;
      color: #fff;
      margin-top: -50px;

      @media (max-width: 600px) {
        font-size: 60px;
        margin-top: -70px;
      }

      @media (max-width: 483px) {
        font-size: 42px;
        margin-top: -90px;
      }

      @media (max-width: 360px) {
        font-size: 38px;
      }
    }

    &__code-container {
      display: flex;

      @media (max-width: 600px) {
        margin-top: -20px;
      }

      @media (max-width: 320px) {
        margin-top: -40px;
      }
    }

    &__code {
      display: flex;
      align-items: center;
      justify-content: center;

      margin-top: 40px;
      padding-left: 15px;
      height: 80px;
      width: 267px;

      border-top: 1px dashed #464646;
      border-bottom: 1px dashed #464646;
      border-left: 1px dashed #464646;

      border-top-left-radius: 40px;
      border-bottom-left-radius: 40px;

      font-family: Arial;
      font-size: 40px;
      line-height: 43.51px;
      color: #f73427;
      letter-spacing: 4px;

      @media (max-width: 1200px) {
        background-color: rgba(0, 0, 0, 0.5);
        border: none;
        border-right: 1px solid #464646;
      }
    }

    &__copy-code {
      display: flex;
      align-items: center;
      justify-content: center;

      margin-top: 40px;
      height: 80px;
      width: 200px;

      border-right: 1px dashed #464646;
      border-left: 1px solid #464646;
      border-top: 1px dashed #464646;
      border-bottom: 1px dashed #464646;

      border-top-right-radius: 40px;
      border-bottom-right-radius: 40px;

      font-family: Arial;
      font-size: 18px;
      line-height: 22px;
      letter-spacing: 1.8px;
      color: #fff;
      cursor: pointer;

      transition: background-color 0.3s ease;

      &:hover {
        background-color: rgba(255, 255, 255, 0.1);
      }

      @media (max-width: 1200px) {
        background-color: rgba(0, 0, 0, 0.5);
        border: none;
      }
    }

    &__button {
      margin-top: 60px;
      height: 80px;
      width: 360px;
      background-color: #f73427;
      color: #fff;

      border-radius: 40px;

      font-family: Arial;
      font-weight: bold;
      font-size: 20px;
      letter-spacing: 2px;

      text-transform: uppercase;
      cursor: pointer;

      transition: color 0.3s ease,
        background-color 0.3s ease,
        transform 0.3s ease;

      @media (max-width: 600px) {
        margin-top: 40px;
      }

      &:hover {
        color: #f73427;
        background-color: #fff;

        -webkit-box-shadow: 0px 0px 50px 20px rgba(0,0,0,0.9);
        -moz-box-shadow: 0px 0px 50px 20x rgba(0,0,0,0.9);
        box-shadow: 0px 0px 50px 20px rgba(0,0,0,0.9);
      }

      &:active {
        transform: scale(0.9);
      }
    }
  }
</style>
