<template>
  <div id="app">
    <nav class="navbar has-shadow" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item">MyCompany</a>
        <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
      <div class="navbar-menu navbar-end">
        <router-link to="/" class="navbar-item r-item">Home</router-link>
        <router-link to="/faq" class="navbar-item r-item">Features</router-link>
        <router-link to="/faq" class="navbar-item r-item">About</router-link>
        <router-link to="/faq" class="navbar-item r-item">FAQ</router-link>

        <div class="navbar-item">
          <p class="control">
            <a class="button is-primary is-outlined">
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
  </div>
</template>

<script>
export default {
  name: 'App'
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
</style>
