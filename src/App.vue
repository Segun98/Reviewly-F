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
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;600&display=swap");

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
  font-family: "Quicksand", sans-serif !important;
  background: var(--background);
}

a {
  text-decoration: none;
  font-weight: 600;
  &:hover {
    text-decoration: none;
  }
}

h1 {
  font-weight: 600;
}
li {
  list-style: none;
}
</style>
