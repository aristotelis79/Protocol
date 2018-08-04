<template>
  <div>
    <div class="header-background">
      <section class="hero is-info is-medium is-bold">
        <!-- Hero content: will be in the middle -->
        <div class="hero-body">
          <div class="container has-text-centered">
            <h1 class="title is-1">
              Protocol
            </h1>
          </div>
          <br>
          <div class="block has-text-centered">
            <a class="button" href="#">
              <span class="icon">
                <i class="fab" />
              </span>
              <span>Start</span>
            </a>
          </div>
        </div>
      </section>
    </div>
    <div class="section">
      <system-information v-show="isDev()" />
    </div>
  </div>
</template>

<script>
import SystemInformation from './Home/SystemInformation'

export default {
  name: 'Home',

  components: { SystemInformation },

  methods: {
    isDev() {
      return process.env.NODE_ENV === 'development'
    }
  }
}
</script>

<style>
.header-background {
  background: rgb(255, 255, 255); /* Old Browsers */
  background: -webkit-radial-gradient(
    center,
    rgb(255, 255, 255),
    rgb(0, 122, 205)
  ); /*Safari 5.1-6*/
  background: -o-radial-gradient(
    center,
    rgb(255, 255, 255),
    rgb(0, 122, 205)
  ); /*Opera 11.1-12*/
  background: -moz-radial-gradient(
    center,
    rgb(255, 255, 255),
    rgb(0, 122, 205)
  ); /*Fx 3.6-15*/
  background: radial-gradient(
    ellipse at center,
    rgb(255, 255, 255),
    rgb(0, 122, 205)
  ); /*Standard*/
}
</style>
