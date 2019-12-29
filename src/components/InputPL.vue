<template>
  <div class="label_input">
    <label :for="forLabel">{{ textLabel }}:</label>
    <input :type="typeInput" :name="nameInput" :id="idInput" />
  </div>
</template>

<script>
export default {
  name: "input-element",
  props: {
    forLabel: {
      type: String,
      default: "default"
    },
    textLabel: {
      type: String
    },
    typeInput: {
      type: String
    },
    nameInput: {
      type: String
    },
    idInput: {
      type: String,
      default: "default"
    }
  }
};
</script>

<style lang="scss" scoped>
$base-color: whitesmoke;

.label_input {
  // width: 100%;
  margin-right: 0;
  background: $base-color;
  padding: 10px 20px 10px 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
label {
  margin: 10px 0 10px 0;
}
input {
  width: 90%;
  height: 30px;
  padding: 10px;
  margin-top: 5px;
  margin-bottom: 5px;
  font-size: 15px;
  border: 1px solid white;
  text-align: center;
}
</style>
