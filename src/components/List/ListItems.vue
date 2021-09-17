<template>
  <ul class="list__items">
    <li class="list__item" v-for="todo in todos" :key="todo.id">
      <input
        type="checkbox"
        id="check"
        :checked="todo.status === 'completed'"
      />
      <label for="check" class="list__check">
        <img src="../../assets/icon-check.svg" alt="" />
      </label>
      <span class="list__value">{{ todo.name }}</span>
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
