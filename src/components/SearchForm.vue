<template>
  <div class="search-wrap text-center" :style="Bimage">
    <div class="search-wrap_form">
      <p class="label">
        Largest source of Apartment Reviews and Prices in Lagos
      </p>
      <b-form @submit="onSubmit">
        <b-form-group id="input-group-1">
          <b-form-input
            aria-label="Find Apartments by Address, LCDA or Name"
            id="input-1"
            v-model="search"
            type="search"
            placeholder="Find apartments by Address, LCDA or Name"
            required
          ></b-form-input>
        </b-form-group>
        <b-button type="submit" class="search-btn">Search</b-button>
      </b-form>
    </div>
  </div>
</template>

<script>
// import Background from "@/assets/header1.jpg";
export default {
  name: "SearchForm",
  props: {
    msg: String,
  },
  data() {
    return {
      search: "",
      Bimage: {
        backgroundImage: `url(${require("../assets/header23.jpg")})`,
      },
    };
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      alert(JSON.stringify(this.search));
      this.search = "";
    },
  },
  // watch: {
  //   backgroundSize: (next, prev) => {
  //     console.log(prev);
  //     console.log(next);
  //     console.log("changed");
  //   },
  // },
  // mounted() {
  //   this.backgroundSize = window.screen.width;
  // },
  // created() {
  //   this.backgroundSize = window.screen.width;
  // },
  // updated() {
  //   // console.log("hello");
  //   // console.log(window.screen.width);
  // },
};
</script>

<style lang="scss" scoped>
.search-wrap {
  background-repeat: no-repeat;
  background-size: cover;
  height: 250px;

  &_form {
    margin: auto;
    width: 90%;
    padding-top: 50px;

    .label {
      color: var(--header);
      font-weight: bolder;
      // color: white;
      font-size: 1.1rem;
      letter-spacing: 2px;
      color: white;
    }
  }
  .search-btn {
    background: var(--green);
    border: none;
  }

  @media only screen and (min-width: 700px) {
    height: 350px;
    &_form {
      width: 70%;
      padding-top: 100px;
    }
  }

  @media only screen and (min-width: 1000px) {
    height: 450px;
    background-position-y: -250px;

    &_form {
      width: 50%;
      padding-top: 150px;
      #input-1 {
        padding: 25px;
      }
      .label {
        font-size: 1.5rem;
        // color: white;
      }
    }

    .search-btn {
      padding: 10px 25px;
      font-size: 1.05rem;
    }
  }

  @media only screen and (min-width: 1800px) {
    height: 650px;
    background-position-y: -450px;

    &_form {
      width: 40%;
      padding-top: 250px;
      #input-1 {
        padding: 26px;
        margin-top: 10px;
      }
      .label {
        font-size: 1.8rem;
      }
    }

    .search-btn {
      padding: 13px 30px;
      font-size: 1.1rem;
    }
  }
}
</style>