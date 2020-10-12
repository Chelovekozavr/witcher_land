<template>
  <div class="images">
    <img
      src="../assets/images/witcher.png"
      alt="Witcher"
      class="witcher"
    >
    <img
      src="../assets/images/sparks_back_blured.png"
      alt="sparks"
      class="sparks-back-blured"
    >
    <img
      src="../assets/images/sparks_back.png"
      alt="sparks"
      class="sparks-back"
    >
  </div>
</template>

<script>
  export default {

  }
</script>

<style lang="scss" scoped>
  .images {
    @media (max-width: 1200px) {
      display: flex;
      justify-content: center;
      align-items: end;

      width: 100vw;
      height: 100vh;
    }
  }

  .witcher {
    left: 68px;
    top: -29px;

    z-index: 2;
    transform: scale(0.95);

    @media screen and (orientation: portrait) and (max-width: 1366px) {
      margin-top: 200px;
      transform: scale(1.3);
    }

    @media (max-width: 480px) {
      transform: scale(0.6);
      margin-top: -90px;

      position: inherit;
    }

    @media (max-width: 320px) {
      transform: scale(0.5);
      margin-top: -250px;
    }
  }

  .sparks-back-blured {
    position: absolute;
    left: -100px;
    top: 20px;
    filter: blur(5px);

    animation-name: sparks-back-blured;
    animation-duration: 30s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;

    z-index: 3;
  }

  .sparks-back {
    position: absolute;
    left: -50px;
    top: -40px;

    animation-name: sparks-back;
    animation-duration: 30s;
    animation-iteration-count: infinite;
    animation-timing-function: ease;
    z-index: 1;
  }

  @keyframes sparks-back-blured {
    0% {
      top: -40px;
      transform: scale(0.8);
    }
    100% {
      top: -400px;
      transform: scale(1);
    }
  }

  @keyframes sparks-back {
    0% {
      transform: scale(0.8);
    }
    100% {
      transform: scale(1);
    }
  }
</style>
