<template>
  <div class="todo-item"  >
    <div class="todo-item-content">
      <span class="data">{{item.content}}</span>
    </div>
    <span class="delete-btn" title="delete" v-on:click.stop="onDelete"></span>
  </div>
</template>

<script>
export default {
  name: "Item",
  props: ["item"],
  methods: {
    onDelete: function() {
      this.$emit("item-delete");
    }
  }
};
</script>

<style scoped>

</style>