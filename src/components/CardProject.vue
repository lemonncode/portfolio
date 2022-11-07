<template>
   

    <div class="bg-pink-300 h-96 w-96 border-solid border-2" >
        <h1>Titulo: {{ title}}</h1>
        <p>Descripción: {{description}}</p>
        <img :src="image">
      </div>
  
</template>

<script>
export default {
  name: "CardProject",
  props:['title', 'description', 'image'],
  data(){
    return{
       /*image: "https://picsum.photos/id/237/300/200"
        https://i.picsum.photos/id/16/2500/1667.jpg?hmac=uAkZwYc5phCRNFTrV_prJ_0rP0EdwJaZ4ctje2bY7aE
        https://i.picsum.photos/id/25/5000/3333.jpg?hmac=yCz9LeSs-i72Ru0YvvpsoECnCTxZjzGde805gWrAHkM
        https://i.picsum.photos/id/37/2000/1333.jpg?hmac=vpYLNsQZwU2szsZc4Uo17cW786vR0GEUVq4icaKopQI


       */
    }
  },

  methods: {
   
  },
};
</script>

<style>

</style>