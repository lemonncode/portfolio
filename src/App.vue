<template >
  <div>
    <h1>Noelia Morlio - portfolio</h1>
    <button @click="isAdmin = true" class="bg-red-200 border">ADMIN</button>
    <button @click="isAdmin = false" class="bg-blue-200 border">USER</button>
    <admin-view v-if="isAdmin" @createProject="addProject" />
    <user-view v-else @createProject="addProject" />
    <div class="bg-amber-200 grid grid-cols-3">
      <card-project
        v-for="project in allProjects"
        :key="project.title"
        :title="project.title"
        :description="project.description"
        :image="project.image"
      ></card-project>
    </div>
  </div>
</template>

<script>
import AdminView from "./components/AdminView.vue";
import CardProject from "./components/CardProject.vue";
import UserView from "./components/UserView.vue";

export default {
  name: "App",
  components: {
    userView: UserView,
    adminView: AdminView,
    CardProject,
  },
  data() {
    return {
      isAdmin: true,
      allProjects: [],
    };
  },
  methods: {
    addProject(project) {
      this.allProjects.push(project);
    },
  },
};
</script>

<style></style>
