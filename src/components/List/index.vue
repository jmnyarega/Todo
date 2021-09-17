<template>
  <section class="list">
    <ListItems :todos="todos" />
    <div class="status-bar">
      <a href="#0" class="status-bar__left">5 items left</a>
      <ul class="status-bar__filter">
        <li><a class="all -active" href="">all</a></li>
        <li><a class="active" href="">active</a></li>
        <li><a class="completed" href="">completed</a></li>
      </ul>
      <a href="#0">clear completed</a>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import ListItems from "./ListItems.vue";

@Component({
  components: {
    ListItems,
  },
  data() {
    return {
      todos: [
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint, quasi. ",
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint, quasi. ",
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint, quasi. ",
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint, quasi. ",
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint, quasi. ",
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint, quasi. ",
      ],
    };
  },
})
export default class Lists extends Vue {}
</script>
