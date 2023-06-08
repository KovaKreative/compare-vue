<template>
  <div id="app">
    <nav class="navbar has-shadow" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item">MyCompany</a>
        <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" v-on:click="toggleNav"
          v-bind:class="{ 'is-active': isActive }">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
      <div class="navbar-menu navbar-end" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
        <router-link to="/" class="navbar-item r-item">Home</router-link>
        <router-link to="/faq" class="navbar-item r-item">Features</router-link>
        <router-link to="/faq" class="navbar-item r-item">About</router-link>
        <router-link to="/faq" class="navbar-item r-item">FAQ</router-link>

        <div class="navbar-item">
          <p class="control">
            <a class="button is-warning is-outlined">
              <span class="icon">
                <i class="fa fa-download"></i>
              </span>
              <span>Join Now</span>
            </a>
          </p>
        </div>
      </div>
    </nav>
    <router-view />
    <footer class="footer">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>This is the footer which can give you some information.</p>
          </div>
          <div class="column has-text-right">
            <a class="icon" href="#"><i class="fa fa-facebook"></i></a>
            <a class="icon" href="#"><i class="fa fa-twitter"></i></a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      isActive: false
    };
  },
  methods: {
    toggleNav: function() {
      this.isActive = !this.isActive;
    }
  }
};
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq'
.navbar
  background-color: #353540
  a:hover
    color: gray

.navbar-brand a
  color: #fed
  font-weight: bold

a.r-item
  color: #C1C1C1
  padding: 0.5rem 1.75rem
  +mobile
    color: gray
    &:hover
      background-color: #F1F1F5

.navbar-burger span
  backbround-color: #C1C1C5

footer
  background-color: $warning !important
  color: $dark

  .icon
    color: $dark
    margin-left: 1em
    font-size: 32px

</style>
