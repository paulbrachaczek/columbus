<template>
  <div id="app">
    <Header :items="items" :summary="summary"/>
    <Main @update="update"/>
    <Footer/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Header from './layout/Header.vue';
import Footer from './layout/Footer.vue';
import Main from './layout/Main.vue';

@Component({
  components: {
    Header,
    Footer,
    Main
  }
})
export default class App extends Vue {
  items = 0;
  summary = 0;

  update(price: number) {
    this.items += 1;
    this.summary += price;
  }
}


</script>

<style lang="scss">
@import '@/assets/scss/style.scss';
#app {}
</style>
