<template>
  <div>
    <item
      v-for="(item) in todo.items"
      v-bind:key="item.id"
      v-bind:item="item"
      v-on:item-delete="onDelete(item)"
    ></item>
  </div>
</template>

<script>
import Item from "./Item";

export default {
  name: "AllItems",
  props: ["todo"],
  components: {
    item: Item
  },
  methods: {
    onDelete: function(item) {
      this.todo.delete(item);
    }
  }
};
</script>

<style scoped>
</style> 
