<template>
  <div v-for="project in projects" :key="project.title">
    <div
      class="
        bg-neutral-100
        h-96
        w-96
        border-solid border-4 border-neutral-100
        hover:bg-neutral-50
        shadow-2xl
        rounded-xl
      "
    >
      <div>
        <img class="rounded-t-lg drop-shadow-xl" :src="project.image" />
      </div>
      <div class="bg-pink-200 mx-4 h-12 p-4">
        <h1
          class="
            place-self-center
            m-auto
            font-mono
            text-base
            font-medium
            tracking-widest
            text-slate-700
            decoration-pink-500/30
          "
        >
          Titulo: {{ project.title }}
        </h1>
      </div>
      <div class="bg-pink-200 m-4 h-12 p-4">
        <p
          class="
            place-self-center
            m-auto
            font-mono
            text-xs
            font-medium
            tracking-widest
            text-slate-700
            decoration-pink-500/30
          "
        >
          Descripción: {{ project.description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Asia 2",
          description: "HONG KONG EN BLANCO Y NEGRO",
          image: "src/img/flowers.jpg",
        },
        {
          title: "Asia",
          description: "Hong Kong en 10 palabras – parte I",
          image: "src/img/lotus.jpg",
        },
        {
          title: "Viajando",
          description: "Vietnam: amor a primera vista",
          image: "src/img/pink.jpg",
        },
      ],
    };
  },
};
</script>

<style>
</style>