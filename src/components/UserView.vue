<template>
  <div>
    <div class="bg-neutral-200 flex h-full">
      <h1
        class="
          place-self-center
          m-auto
          font-mono
          text-6xl
          font-medium
          tracking-widest
          text-zinc-500
          decoration-pink-500/30
          mt-10
        "
      >
        Portfolio
      </h1>
      
    </div>

    <div
      class="
        bg-neutral-200
        grid grid-cols-1
        place-items-center
        md:grid-cols-2
        lg:grid-cols-2
        xl:grid-cols-3
        gap-24
        lg:gap-10
        p-12
        
      "
      @click="showDetails"
    >
     
        <project></project>
    
    </div>
  </div>
</template>

<script>
import Project from "./Project.vue";
export default {
  components: { Project },
  name: "UserView",
  data() {
    return {
      project: [
        {
          title: "",
          description: "",
          image: '',
        },
      ],
    };
  },
};
</script>

<style></style>
