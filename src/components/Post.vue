<template>
  <div class="post">
    <img :src="image" alt="image" />
    <div class="post_body">
      <h1>{{ title }} {{ id }}</h1>
      <h3>{{ subtitle }}</h3>
      <hr />
      <p>{{ text.substr(0, 200) + "..." }}</p>
      <div class="footer_post">
        <p class="footer_p">
          Pubblicato il: <br />
          {{ formattedDate }}
        </p>
        <p class="footer_p">
          Autore: <br />
          {{ author }}
        </p>
      </div>

      <router-link class="routers" to="/book">
      <div class="button" @click="details">
        <ButtonPL textButtonPL="Dettagli" />
      </div>
      </router-link>
    </div>
  </div>
</template>

<script>
import dayjs from "dayjs";
import ButtonPL from "@/components/ButtonPL.vue";
// importing bus
import { bus } from "../main";

export default {
  name: "post",
  props: ["subtitle", "title", "author", "image", "date", "text", "id"],
  data() {
    return {
      //   clicked: false
      clickedXcollector: false,
      clickedXinfo: false
    };
  },
  components: {
    ButtonPL
  },
  computed: {
    formattedDate() {
      return dayjs(this.date).format("DD/MM/YYYY");
    }
  },
  methods: {
    details() {
      console.log("id articolo: " + this.id, "title: " + this.title);
      this.clickedXinfo = true;
      // this.$router.push({ path: `/post/${this.id}` });
      // this.$root.$emit("details", this.id);

      // use bus
      bus.$emit("changeStuff", this.title);
    }
  }
};
</script>
<style lang="scss" scoped>
$base-color: #d0e8f9;

.post {
  // border: 1px solid red;

  margin: 10px 0;
  padding: 10px;
  // background: gainsboro;
  box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.2);
  // border-radius: 10px
  // position: relative;
  // top: 40px
}
.post_body {
  padding: 0 15px 10px 15px;
  background: whitesmoke;
  // margin: 10px;
  padding: 20px;
  // border-radius: 10px

  //// accorciare il testo
  //   white-space: nowrap;
  //   width: 50%;
  //   overflow: hidden;
  //   text-overflow: ellipsis;
}
img {
  width: 100%;
  margin-bottom: 10px;
  // border-radius: 10px
}
h1 {
  margin: 0;
}

.footer_post {
  display: flex;
  justify-content: space-between;
}

.footer_p {
  font-size: 14px;
}

.button {
  margin-top: 20px;
  margin-bottom: 10px;
}
</style>
