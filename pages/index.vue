<template>
  <div class="main">
    <div class="container">
      <div class="home">
        <div class="home-section left">
          <h2 class="h2 with-shadow">
            ONESECOND.CC
          </h2>
          <p class="text home-text">
            New type of online services where artists can get professional support
            in recording & distribution, promoting music, get funding for projects
          </p>
          <nuxt-link
            to="/form"
            class="button-o2 home-button"
          >
            join one second
          </nuxt-link>
        </div>
        <div class="home-section right">
          <img
            class="home-image"
            src="~/assets/images/girl2.png"
            alt="girl"
          >
        </div>
      </div>
      <Microphones class="home-mics" />
      <Database class="home-database" />
    </div>
    <div>
      <Mobile class="home-mobile" />
      <Promo class="home-promo" />
      <Artists class="home-artists" />
      <Footer class="home-footer" />
    </div>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue';
  import Microphones from '../components/landing/Microphones.vue';
  import Artists from '../components/landing/Artists.vue';
  import Database from '../components/landing/Database.vue';
  import Mobile from '../components/landing/Mobile.vue';
  import Promo from '../components/landing/Promo.vue';
  import Footer from '../components/landing/Footer/Footer.vue';
  export default Vue.extend({
    components: {
      Artists,
      Database,
      Footer,
      Microphones,
      Mobile,
      Promo
    }
  });
</script>

<style scoped lang="scss">
@import "../assets/styles/base/variables";

.main {
  overflow: hidden;
  @media($mobile) {
    overflow-x: hidden;
  }

}

.container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.home {
  display: flex;
  width: 100%;

  @media($tablet) {
    flex-direction: column-reverse;
    overflow-x: hidden;
  }

  @media($mobile) {
    width: 100%;
    overflow-x: hidden;
  }

  // components sections

  &-mics {
    margin-top: 150px;
  }

  &-database {
    @media($desktop) {
      margin-top: 150px;
    }

    @media($tablet) {
      margin-top: 650px;
    }

    @media($mobile) {
      margin-top: 400px;
    }
  }

  &-mobile {
    margin-top: 250px;
    @media ($tablet) {
      margin-top: 100px;
    }
    @media($mobile) {
      margin-top: 150px;
    }
  }

  &-promo {
    margin-top: 100px;

    @media ($tablet) {
      min-height: auto;
      margin-top: 50px;
    }

    @media($mobile) {
      margin-top: 50px;
    }
  }

  &-artists {
    margin-top: 100px;
    @media ($desktop) {
      margin-top: 50px;
    }

    @media($mobile) {
      margin-top: 50px;
    }
  }
  // components sections

  &-section {
    flex: 1;
    position: relative;
    align-items: center;

    &.left {
      padding-top: 150px;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      animation: opacity 1s ease-in-out;

      @media($tablet) {
        margin-top: 630px;
        padding: 0 40px;
      }

      @media($mobile) {
        margin-top: 380px;
        padding: 0 20px 0 20px;
      }
    }
  }

  &-button {
    margin-top: 80px;

    @media($tablet) {
      margin-top: 40px;
    }

    @media($mobile) {
      margin-top: 30px;
    }
  }

  &-image {
    position: absolute;
    left: -240px;
    min-width: 1140px;
    animation: slideUp 1s ease-in-out, opacity 1.5s ease-in-out;

    @media($tablet) {
      left: -190px;
    }

    @media($mobile) {
      min-width: 150%;
      max-width: 150%;
      left: 0;
      transform: translateX(-16%);
    }
  }

  &-text {
    max-width: 480px;
    line-height: 120%;
    @media($mobile) {
      max-width: 300px;
    }
  }
}

</style>
