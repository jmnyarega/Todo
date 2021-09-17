<template>
  <div class="u-container">
    <Header />
    <Input />
    <Lists />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Header from "./components/Header.vue";
import Input from "./components/Input.vue";
import Lists from "./components/List/index.vue";

@Component({
  components: {
    Header,
    Input,
    Lists,
  },
})
export default class App extends Vue {}
</script>

<style src="./css/index.scss" lang="scss" />
