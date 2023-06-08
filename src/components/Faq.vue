<template>
  <div class="faq">
    <div class="container">
      <section class="section">
        <h1 class="title">FAQ</h1>
        <h2 class="subtitle is-4">Lorem ipsum etc.</h2>
        <div class="columns" v-if="faqs && faqs.length">
          <div class="column is-one-third" v-for="faq of faqs">
            <div class="card">
              <div class="card-content">
                <p class="title">{{ faq.title }}</p>
                <p class="answer">{{ faq.body }}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Faq',
  data: () => ({
    faqs: [],
    errors: []
  }),
  created() {
    axios.get('https://jsonplaceholder.typicode.com/posts')
      .then(res => {
        console.log(res);
        this.faqs = res.data.slice(0, 10);
      })
      .catch(err => {
        this.errors.push(err);
      });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../mq'

.pd
  padding: 2.5em 0 1.5em 0
.answer
  margin-top: 10px
  color gray
.columns
  flex-wrap: wrap
  align-items: stretch
  
</style>
