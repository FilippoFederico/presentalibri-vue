<template>
  <div class="buttonPL">
    <button :type="typeButtonPL" :value="valueButtonPL">
      {{ textButtonPL }}
    </button>
  </div>
</template>

<script>
export default {
  name: "button-pl",
  props: {
    textButtonPL: {
      type: String,
      default: "Click here!"
    },
    typeButtonPL: {
      type: String
    },
    valueButtonPL: {
      type: String
    }
  }
};
</script>

<style lang="scss" scoped>
.buttonPL {
  background: gainsboro;
  height: 25px;
  padding: 10px 10px;
  text-align: center;
  display: flex;
}
button {
  font-size: 15px;
  background: transparent;
  border: none;
}
</style>
