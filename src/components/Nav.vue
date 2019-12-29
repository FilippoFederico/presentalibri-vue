<template>
  <nav>
    <router-link class="routers" to="/"
      ><div class="logo">
        <p class="logo_name">presentalibri</p>
        <small>libri libri libri libri</small>
      </div></router-link
    >
    <div class="menu">
      <div @click="toggleDropdown">
        <ButtonPL textButtonPL="menu" />
      </div>
      <!-- <button>menu</button> -->
      <div class="dropdown" :class="{ visible: visible }">
        <ul>
          <router-link class="routers" to="/book"><li>book</li></router-link>
          <!-- <router-link class="routers" to="/events/"><li>blog eventi</li></router-link> -->
          <router-link class="routers" to="/contact/"
            ><li>contatti</li></router-link
          >
        </ul>
      </div>
    </div>
  </nav>
</template>
<script>
import ButtonPL from "@/components/ButtonPL.vue";

export default {
  name: "navbar",
  components: {
    ButtonPL
  },
  data() {
    return {
      visible: false
    };
  },
  methods: {
    toggleDropdown() {
      this.visible = !this.visible;
    }
  }
};
</script>
<style lang="scss" scoped>
$box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.2);

nav {
  // border: 1px solid red;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 30px;
  background: whitesmoke;
  position: sticky;
  top: 6px;
  z-index: 2;
  box-shadow: $box-shadow;
}
.logo {
  // border: 1px solid red;
  padding: 10px 0;
}
.logo_name {
  font-size: 30px;
  padding: 0;
  margin: 0;
}
.menu {
  // border: 1px solid red;
  position: relative;
}
button {
  // border: 1px solid red;
  background: LightSlateGray;
}
.dropdown {
  display: none;
  position: absolute;
  right: 0;
  text-align: right;
  background: white;
  border-radius: 5px;
  padding: 0 10px;
  top: 50px;
  box-shadow: 0 0 3px 0 rgba(0, 0, 0, 0.2);
  min-width: 80px;
  z-index: 1;

  &.visible {
    display: block;
  }
  @media (min-width: 768px) {
    position: static;
    display: block;
  }
}
ul {
  // border: 1px solid red;
  list-style: none;
  padding: 0;
  width: 100%;
}
li {
  border-bottom: 1px solid gainsboro;
  padding: 8px 0;
}
.routers {
  text-decoration: none;
  color: black;
}
</style>
