<template>
  <div>
    <form action="">
      <div>
        <InputPL
          forLabel="firstname"
          textLabel="Nome"
          typeInput="text"
          nameInput="firstname"
          idInput="firstname"
        />
      </div>
      <div>
        <InputPL
          forLabel="lastname"
          textLabel="Cognome"
          typeInput="text"
          nameInput="lastname"
          idInput="lastname"
        />
      </div>
      <div>
        <InputPL
          forLabel="mail"
          textLabel="Mail"
          typeInput="mail"
          nameInput="mail"
          idInput="mail"
        />
      </div>
      <div class="textarea">
        <label class="label_textarea" for="textarea">Text area:</label>
        <textarea name="message" rows="10" cols="30" id="textarea"></textarea>
      </div>
      <div class="button">
        <ButtonPL
          textButtonPL="Submit"
          typeButtonPL="submit"
          valueButtonPL="submit"
        />
      </div>
    </form>
  </div>
</template>

<script>
import InputPL from "@/components/InputPL.vue";
import ButtonPL from "@/components/ButtonPL.vue";

export default {
  name: "form-component",
  components: {
    InputPL,
    ButtonPL
  }
};
</script>

<style lang="scss" scoped>
$base-color: whitesmoke;
$box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.2);

form {
  width: 100%;
}

.form_input {
  margin-right: 0;
  background: $base-color;
  padding: 10px 20px 10px 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
input {
  width: 90%;
  height: 30px;
  padding: 10px;
  margin-top: 5px;
  margin-bottom: 5px;
  font-size: 15px;
  border: 1px solid white;
}
label {
  margin: 10px 0 10px 0;
}
.textarea {
  background: $base-color;
  padding: 10px 20px 10px 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

textarea {
  width: 90%;
  padding: 10px;
  font-size: 15px;
  border: 1px solid white;
  margin-top: 5px;
  margin-bottom: 5px;
}
button {
  border: 1px solid white;
  width: 60%;
  height: 40px;
  justify-content: center;
  margin-top: 20px;
  margin-bottom: 20px;
}
.button {
  padding-top: 20px;
  padding-bottom: 10px;
  display: flex;
  justify-content: center;
  background: $base-color;
  // background: $base-color
}
</style>
