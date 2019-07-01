<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 offset-md-3">
        <div class="form-group d-flex">
          <input
            type="text"
            class="form-control"
            placeholder="Add New Task"
            aria-describedby="helpId"
            v-model="title"
          />
          <button
            type="submit"
            @click.prevent="submitForm"
            class="btn btn-primary btn-block mb-4"
          >Submit</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  data() {
    return {
      title: ""
    };
  },
  methods: {
    ...mapActions(["addTodo"]),
    submitForm() {
      this.addTodo(this.title);
      this.title = "";
    }
  }
};
</script>

<style>
</style>
