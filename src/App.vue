<template >
  <div class=" bg-neutral-50">
    <div
      class="
        gap-4
        bg-zinc-300
        h-32
        w-full
        flex flex-row
        justify-around
        pt-4
        drop-shadow-lg
        pr-20
        
        
      "
    >
      <Header></Header>
      <button
        @click="isAdmin = true"
        class="
          bg-neutral-100
          hover:bg-neutral-400
          text-gray-800
          py-2
          px-4
          border border-neutral-500
          rounded
          shadow
          h-12
        "
      >
        <h1 class="font-mono text-lg font-medium">admin</h1>
      </button>
      <button
        @click="isAdmin = false"
        class="
          bg-neutral-100
          hover:bg-neutral-400
          text-gray-800
          py-2
          px-4
          border border-neutral-500
          rounded
          shadow
          h-12
        "
      >
        <h1 class="font-mono text-lg font-medium">user</h1>
      </button>
    </div>
    <admin-view v-if="isAdmin" @createProject="addProject" />
    <user-view v-else @createProject="addProject" />
    <div class="
        bg-neutral-200
        grid grid-cols-1
        place-items-center
        md:grid-cols-2
        lg:grid-cols-2
        xl:grid-cols-3
        gap-24
        lg:gap-10
        p-12
        
        
      ">
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
import Header from "./components/globo/Header.vue";

export default {
  name: "App",
  components: {
    userView: UserView,
    adminView: AdminView,
    CardProject,
    Header,
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
