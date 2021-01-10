<template>
  <section>
    <Search msg="hello from search! I love Vue" />
  </section>
</template>

<script>
import Search from "@/components/Search.vue";

export default {
  name: "Home",
  components: {
    Search,
  },
};
</script>

<style lang="scss" scoped>
</style>
