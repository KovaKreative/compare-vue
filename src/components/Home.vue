<template>
  <div class="home">
    <section class="hero is-medium is-warning">
      <div class="hero-body">
        <h1 class="title">
          {{ heading }}
        </h1>
        <div class="is-three-quarters column is-paddingless">
          <h2 class="subtitle is-4">
            {{ subheading }}
          </h2>
        </div>
        <a class="button is-large is-dark" id="learn">Learn More</a>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <div class="columns pd is-desktop">
          <div class="column is-1 has-text-centered">
            <i class="fa fa-cog is-link"></i>
          </div>
          <div class="column is-one-third-desktop">
            <p class="title"><strong>Full Stack Web Developer experienced in education and game design.</strong></p>
          </div>
          <div class="column">
            <p>A passionate designer and developer, driven to create efficient applications that provide an engaging and intuitive user experience.</p>
          </div>
        </div>
      </div>
      <div class="columns pd">
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">I have always been a creative person with a particular affinity for computer technology and expressing myself through it.</p>
              <p class="subtitle">-Eric Kovalevskyy</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">I have a particular passion for video games, which marry storytelling, cinematography, visual arts, and music, and deliver engaging, interactive experiences. </p>
              <p class="subtitle">-Eric Kovalevskyy</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">I have always aspired to leverage these principles to deliver user experiences that allow for expression and creativity in engaging and intuitive ways.</p>
              <p class="subtitle">-Eric Kovalevskyy</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      heading: 'KovaKreative',
      subheading: 'Full Stack Web Developer experienced in education and game design. A passionate designer and developer, driven to create efficient applications that provide an engaging and intuitive user experience.'
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../mq'
@import '../../node_modules/bulma/bulma.sass'

.hero
  background: url('../assets/subtle-prism.svg')
  background-size: cover

  .title
    +mobile
      font-weight: bold
    +tablet
      font-size: 2.5rem
    +desktop
      font-size: 4rem
      margin-top: 2rem
h2
  margin: 1.5rem 0 2rem 0

.fa-cog
  font-size: 40px

#learn
  +desktop
    margin-bottom: 2rem

.pd
  +tablet
    padding: 2em 0

</style>
