<template>
  <ul class="list__items">
    <li class="list__item" v-for="(todo, key) in todos" :key="key">
      <input type="checkbox" id="check" />
      <label for="check" class="list__check">
        <img src="../../assets/icon-check.svg" alt="" />
      </label>
      <span class="list__value">{{ todo }}</span>
      <span class="list__delete">
        <img src="../../assets/icon-cross.svg" alt="" />
      </span>
    </li>
  </ul>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  props: {
    todos: Array,
  },
})
export default class ListItems extends Vue {}
</script>
