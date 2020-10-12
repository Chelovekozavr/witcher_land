<template>
  <div id="app">
    <main>
      <WitcherPromo />
      <Witcher />
    </main>
    <footer>
      <WitcherFooter />
    </footer>
  </div>
</template>

<script>
  import Witcher from './components/Witcher.vue';
  import WitcherPromo from './components/WitcherPromo.vue';
  import WitcherFooter from './components/WitcherFooter.vue';

  export default {
    name: 'App',
    components: {
      Witcher,
      WitcherPromo,
      WitcherFooter
    }
  }
</script>

<style lang="scss">
  * {
    box-sizing: border-box;
  }

  body {
    margin: 0;
  }

  h1, h2, h3 {
    margin: 0;
  }

  button {
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;

    outline: none;
    border: none;
  }

  @font-face {
    font-family: 'Cambria';
    src: url('./assets/fonts/cambriab.ttf');
  }

  #app {
    height: 100vh;
    width: 100vw;
    background-color: #000;

    background: url(./assets/images/bg.png) top center;
    background-size: cover;
    -moz-background-size: cover;
    -webkit-background-size: cover;
    -o-background-size: cover;
    background-repeat: no-repeat;

    animation-name: fire-contrast;
    animation-duration: 5s;
    animation-iteration-count: infinite;
    
    overflow: hidden;
  }

  @keyframes fire-contrast {
    0% {
      filter: contrast(1);
    }

    50% {
      filter: contrast(1.1);
    }

    100% {
      filter: contrast(1);
    }
  }
</style>
