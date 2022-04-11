<template>
  <form class="form" @submit.prevent="addTodo()">
    <input
      v-model="newTodo"
      type="text"
      class="input"
      placeholder="to-do..."
    />
  </form>
</template>

<script>
export default {
  data() {
    return {
      newTodo: ""
    };
  },
  methods: {
    addTodo() {
      if (this.newTodo.length > 0) {
        this.$emit("on-new-todo", this.newTodo);
      }
      this.newTodo = "";
    }
  }
};
</script>

<style lang="scss" scoped></style>
