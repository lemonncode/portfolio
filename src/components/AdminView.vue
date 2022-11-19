<template >
  <div class=" bg-neutral-50 ">
    <div
      class="
        bg-neutral-200
        border-solid border-2
        h-16
        w-96
        m-auto
        flex
        rounded-lg
        relative
        z-10
        mt-10
      "
    >
      <div class="absolute h-14 w-14 -left-4 -top-5 bg-pink-300 z-20"></div>
      <div class="absolute h-12 w-12 -right-4 -bottom-4 bg-pink-300 z-20">
        <div class="ml-3 mt-3">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M12 6v12m6-6H6"
            />
          </svg>
        </div>
      </div>
      <h1
        class="
          place-self-center
          m-auto
          font-mono
          text-lg
          font-medium
          tracking-widest
          text-slate-700
          decoration-pink-500/30
        "
      >
        Add New Project
      </h1>
    </div>
    <div
      class="
        bg-neutral-200
        shadow-2xl
        border-solid border-8 border-pink-200
        h-96
        w-96
        m-auto
        grid grid-cols-2 grid-rows-5
        mt-16
      "
    >
      <div class="mx-auto mt-4">
        <h1
          class="
            place-self-center
            m-auto
            font-mono
            text-sm
            font-medium
            tracking-widest
            text-slate-700
            decoration-pink-500/30
          "
        >
          project title
        </h1>
      </div>
      <div class="mx-auto mt-4">
        <h1
          class="
            place-self-center
            m-auto
            font-mono
            text-sm
            font-medium
            tracking-widest
            text-slate-700
            decoration-pink-500/30
          "
        >
          image url
        </h1>
      </div>
      <div class="mx-auto">
        <input
          v-model="title"
          class="border h-8 w-40 hover:border-2 hover:border-neutral-500"
        />
      </div>
      <div class="mx-auto">
        <input
          v-model="image"
          class="border h-8 w-40 hover:border-2 hover:border-neutral-500"
        />
      </div>
      <div class="col-span-2 m-auto">
        <h1
          class="
            place-self-center
            m-auto
            font-mono
            text-sm
            font-medium
            tracking-widest
            text-slate-700
            decoration-pink-500/30
          "
        >
          project description
        </h1>
      </div>
      <div class="col-span-2 m-auto hover:border-2 border-neutral-500">
        <input v-model="description" class="border h-16 w-80" />
      </div>
      <div class="place-self-center col-span-2">
        <div class="col-span-2">
          <button
            @click="handleSubmit"
            class="
              bg-neutral-100
              hover:bg-neutral-400
              text-gray-800
              py-2
              px-4
              border border-neutral-500
              rounded
              shadow
            "
          >
            <h1 class="font-mono text-lg font-medium">submit</h1>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AdminView",
  data() {
    return {
      title: "",
      image: "https://picsum.photos/900/600",
      description: "",
    };
  },
  methods: {
    handleSubmit() {
      this.$emit("createProject", {
        title: this.title,
        image: this.image,
        description: this.description,
      });
      (this.title = ""), (this.image = ""), (this.description = "");
    },
  },
};
</script>

<style></style>
