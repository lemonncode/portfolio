<template >
  <div>
    <div class="bg-red-200 border-solid border-2 h-16 w-96 m-auto flex">
      <h1 class="place-self-center m-auto">Add New Project</h1>
    </div>
    <div
      class="
        bg-red-200
        border-solid border-2
        h-96
        w-96
        m-auto
        grid grid-cols-2 grid-rows-5
      "
    >
      <div>Project Title</div>
      <div>Image Url</div>
      <div><input v-model="title" class="border" /></div>
      <div>
        <input v-model="image" class="border" />
      </div>
      <div class="col-span-2">project description</div>
      <div class="col-span-2">
        <input v-model="description" class="border h-24 w-96" />
      </div>
      <div class="place-self-center col-span-2">
        <div class="col-span-2 bg-pink-400">
          <button @click="handleSubmit" class="border">SUBMIT</button>
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
      image: "",
      description: "",
    };
  },
  methods: {
    handleSubmit() {
      this.$emit("createProject", {
        title: this.title,
        image: this.image,
        description: this.description,
      })
      this.title= '',
      this.image='',
      this.description=''
      ;
    },
  },
};
</script>

<style></style>
