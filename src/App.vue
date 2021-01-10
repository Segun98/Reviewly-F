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

body {
  font-family: "Open Sans", sans-serif;
}

:root {
  --primary: #805ad5;
  --header: #333333;
  --subhead: #1f2c35;
  --text: #889ab4;
  --background: #fafafb;
  --pink: #f082ac;
  --green: #2cc096;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
