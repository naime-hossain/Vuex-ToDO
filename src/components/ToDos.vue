<template>
  <div id="todo_wraper">
    <div class="container">
      <div class="row">
        <div class="col-md-6 offset-md-3">
          <ul class="list-group">
            <li
              v-for="(todo,index) of allTodos"
              :key="todo.id"
              class="list-group-item d-flex justify-content-between align-items-center"
              :class="{'active':index==0,'bg-success':todo.completed}"
            >
              {{todo.title}}
              <span class="badge badge-danger badge-pill">Task Number: {{ todo.id }}</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from "vuex";
export default {
  data() {
    return {};
  },
  methods: {
    ...mapActions(["fetchTodos"])
  },
  computed: mapGetters(["allTodos"]),
  created() {
    this.fetchTodos();
  }
};
</script>

<style>
</style>
