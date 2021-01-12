<template>
  <section>
    <Search />
    <Location />
    <TopRated />
    <section class="your-apartment">
      <h1>List Your Apartment with us</h1>
      <div @click="goto">go</div>
      <b-button>Get Started</b-button>
      <router-link to="/about"> down</router-link>
    </section>
  </section>
</template>

<script>
import Search from "@/components/SearchForm.vue";
import Location from "@/components/Location.vue";
import TopRated from "@/components/TopRated.vue";

export default {
  name: "Home",
  components: {
    Search,
    Location,
    TopRated,
  },
  methods: {
    goto() {
      this.$router.push("/about").then(() => window.scrollTo(0, 0));
    },
  },
};
</script>

<style lang="scss" scoped>
.your-apartment {
  text-align: center;
}
</style>
