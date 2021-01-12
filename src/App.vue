<template>
  <div id="app">
    <Header />
    <router-view />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";

export default {
  components: {
    Header,
  },
};
</script>
<style lang="scss" global>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;1,300;1,400&display=swap");
@import url("https://fonts.googleapis.com/css2?family=East+Sea+Dokdo&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;1,100;1,300;1,400&display=swap");

:root {
  --header: #333333;
  --subhead: #1f2c35;
  --text: #889ab4;
  --background: #fafafb;
  --pink: #f082ac;
  --green: #2cc096;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  scroll-behavior: smooth;
}
body {
  font-family: "Open Sans", sans-serif;
  font-family: "East Sea Dokdo", cursive;
  font-family: "Roboto", sans-serif !important;
  background: var(--background);
}

a {
  text-decoration: none;
  &:hover {
    text-decoration: none;
  }
}

li {
  list-style: none;
}
</style>
