<template>
  <div class="hero">
    <p>
      La prima vetrina online La prima vetrina online La prima vetrina online
    </p>
    <!-- <button @click="promuoviLibro">promuovi libro</button>
        <button @click="pubblicaEvento">pubblica evento</button> -->
    <img :src="image" alt="image" />
    <div class="overlay"></div>
    <!-- <div class="FormPromoLibro"><FormPromoLibro class="g"/></div> -->
  </div>
</template>
<script>
export default {
  name: "hero",
  components: {},
  props: ["image"]
  // methods: {
  //     promuoviLibro(){
  //         console.log('promuoviLibro()')
  //     },
  //     pubblicaEvento(){
  //         console.log('pubblicaEvento()')
  //     }
  // }
};
</script>
<style lang="scss" scoped>
.FormPromoLibro {
  // position: relative;
  // top: 0px
}
.g {
}
.hero {
  // border: 1px solid red;
  width: 100%;
  height: 300px;
  margin-top: 10px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  position: relative;
  overflow: hidden;
  color: white;
  // z-index: -1;
}
p {
  width: 70%;
  font-size: 20px;
  text-shadow: 2px 2px black;
  letter-spacing: 2px;
}
button {
  background: whitesmoke;
  border-radius: 5px;
  padding: 5px 20px;
  font-size: 12px;
}
img {
  position: absolute;
  object-fit: cover;
  z-index: -1;
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.2);
  z-index: -1;
}
</style>
