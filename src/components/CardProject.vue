<template>
  <div class="h-96 w-96 border-solid border-2">
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
        <img class="rounded-t-lg drop-shadow-xl" :src="image" />
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
          Titulo: {{ title }}
        </h1>
      </div>
      <div class="bg-pink-200 m-4 h-12 p-4">
        <p
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
          Descripción: {{ description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardProject",
  props: ["title", "description", "image"],
  data() {
    return {
      /*"
       
        https://i.picsum.photos/id/25/5000/3333.jpg?hmac=yCz9LeSs-i72Ru0YvvpsoECnCTxZjzGde805gWrAHkM
      

       */
    };
  },

  methods: {},
};
</script>

<style>
</style>