<template>
  <h1>User List</h1>
  

  <div class="row">
    <div class="col-md-6">
      <div class="list-group ">
        <div
          @click="getUser(item.id)"
          v-for="item in users"
          v-bind:key="item"
          class="list-group-item list-group-item-action d-flex justify-content-between"
        >
          <img v-bind:src="item.avatar" class="img-fluid" />
          <div>
            <p>{{ item.first_name }} {{ item.last_name }}</p>
            <p>{{ item.email }}</p>
          </div>
        </div>
      </div>
    </div>
    <div class="col-md-4" v-if="user.id" >
      <div class="card">
        <div class="card-header text-center">
          <img v-bind:src="user.avatar" class="img-fluid " style="border-rounded:50%" alt="">
        </div>
        <div class="card-body text-center">
            <h2>{{user.first_name}} {{user.last_name}}</h2>
            <h4>{{user.email}}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  methods: {
    async getUsers() {
      const resp = await axios.get("https://reqres.in/api/users");
      console.log(this.user);
      console.log(this.user);
      this.users = await resp.data.data;
    },
    async getUser(id) {
      const resp = await axios.get(`https://reqres.in/api/users/${id}`);
      this.validate= true
      this.user = await resp.data.data;
    },
  },
  created() {
    this.getUsers();
  },
  data() {
    return {
      users: [],
      user: []
    };
  },
};
</script>

<style></style>
