<template>
  <div>
    <div class="page_presentation">
      <h1>Contatti</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error
        doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur
        rerum illum odit fugit assumenda rem dolores inventore iste
        reprehenderit maxime! Iusto.
      </p>
    </div>
    <div class="form_div">
      <Form />
    </div>
  </div>
</template>

<script>
import Form from "@/components/FormComponent.vue";

export default {
  metaInfo: {
    title: "contact"
  },
  components: {
    Form
  }
};
</script>
<style lang="scss" scoped>
$base-color: whitesmoke;
$box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.2);

.page_presentation {
  margin-top: 20px;
  margin-bottom: 20px;
  padding: 10px;
}
.form_div {
  box-shadow: $box-shadow;
  padding: 10px;
}
h1 {
  margin-top: 0;
}
</style>
