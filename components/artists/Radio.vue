<template>
  <div class="radio">
    <img
      class="radio-image"
      src="~/assets/images/radio.jpg"
    >
    <div class="radio-content">
      <div class="container">
        <h1 class="h1 h1-white with-shadow is-uppercase radio-header">
          Onesecond.cc
        </h1>
        <h1 class="h1 h1-white with-shadow is-uppercase radio-header">
          is created
        </h1>
        <h1 class="h1 h1-white with-shadow is-uppercase radio-header">
          for you
        </h1>
        <div class="list-o2 radio-list">
          <div
            v-for="item in items"
            :key="item"
            class="list-o2-item radio-list-item"
          >
            <img
              class="list-o2-image"
              src="~/assets/icons/disc.svg"
              alt="disc"
            >
            <p class="text">
              {{ item }}
            </p>
          </div>
          <div class="radio-button">
            <nuxt-link
              to="/form"
              class="button-o2 is-white with-black">
              join one second
            </nuxt-link>
            <img
              class="radio-button-image"
              src="~/assets/icons/circles.svg"
              alt="circles"
            >
          </div>
        </div>
      </div>
    </div>
    <img
      class="radio-circles"
      src="~/assets/icons/circles-grey.svg"
      alt="circles"
    >
  </div>
</template>

<script lang="ts">
  import Vue from 'vue';

  export default Vue.extend({
    data () {
      return {
        items: [
          'get funding for your projects among your friends, fans or random investors',
          'find local studios, producers, clubs and concert halls',
          'buy songs and beats',
          'connect and collaborate with other musicians, djs and bands',
          'get support with management, promotion and distribution'
        ]
      };
    }
  });
</script>

<style scoped lang="scss">
  @import "../../assets/styles/base/variables";
  .radio {
    position: relative;

    &-image {
      position: relative;
      width: 100%;
    }

    &-circles {
      position: relative;
      margin-top: -4px;
      z-index: 0;

      @media ($tablet) {
        max-width: 30%;
      }

      @media($mobile) {
        max-width: 50%;
      }
    }

    &-button {
      display: flex;
      align-items: center;
      margin-top: $building-unit-x6;

      @media($mobile) {
        justify-content: center;
        margin-top: $building-unit-x2;
      }

      &-image {
        margin-left: auto;
        @media($mobile) {
         display: none;
        }
      }
    }

    &-content {
      position: absolute;
      right: 5%;
      top: $building-unit-x12;
      animation: slideUp 1s ease-in-out, opacity 1.5s ease-in-out;

      @media ($tablet) {
        top: $building-unit-x2;
        z-index: 1;
        right: 0;

        .radio-header {
          text-align: right;
          padding-right: $building-unit-x4;
        }
      }

      @media($mobile) {
        .radio-header {
          padding-right: $building-unit-x2;
        }
      }
    }

    &-header:not(last-child) {
      margin-bottom: 0;
    }

    &-list {
      margin-top: $building-unit-x11;

      @media ($tablet) {
        background-color: $black;
        padding: $building-unit-x4;
        margin: $building-unit-x2 $building-unit-x2 0 $building-unit-x2;
        opacity: .9;
      }
      &-item {
        margin-bottom: $building-unit-x4;
        @media($mobile) {
          margin-bottom: $building-unit-x3;
        }

        .text {
          @media($tablet) {
            line-height: 150%;
          }
        }
      }
    }

  }
</style>
