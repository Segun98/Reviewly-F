<template>
  <section class="top-rated">
    <h1><span>Top Rated</span> Apartments in Lagos</h1>
    <div class="top-rated_wrap">
      <div v-for="(l, i) in lcdas" :key="l.id" class="top-rated_item">
        <div class="relative">
          <img :src="l.image" />
          <p>{{ l.name }}</p>
        </div>
        <section>
          <div class="ratings">
            <h6 style="color: rgb(241, 210, 42)">xxxxx</h6>
          </div>
          <span>|</span>
          <div class="reviews">
            <h6>{{ i + Math.floor(Math.random() * 16) + 5 }} reviews</h6>
          </div>
        </section>
      </div>
    </div>
    <div class="link">
      <router-link to="/about">More apartments</router-link>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      lcdas: [
        {
          id: 1,
          name: "John's Space",
          LCDA: "Lagos Mainland",
          image: require("../assets/header1.jpg"),
        },
        {
          id: 2,
          name: "Tola's Space",
          LCDA: "Ikeja",
          image: require("../assets/header2.jpg"),
        },
        {
          id: 3,
          name: "Freddy's Lounge",
          LCDA: "Eti-Osa",
          image: require("@/assets/header3.jpg"),
        },
        {
          id: 4,
          name: "Masaba Close BQ",
          LCDA: "Lekki",
          image: require("../assets/header1.jpg"),
        },
        {
          id: 5,
          name: "New Hall",
          LCDA: "Ifako-Ijaiye",
          image: require("../assets/header23.jpg"),
        },
        {
          id: 6,
          name: "Moremi's Park Lounge",
          LCDA: "Epe",
          image: require("../assets/header3.jpg"),
        },
      ],
    };
  },

  methods: {
    toTop() {},
  },
};
</script>

<style lang="scss" scoped>
.top-rated {
  margin: 20px 0;
  h1 {
    font-size: 1.2rem;
    color: var(--header);
    text-align: center;
    font-weight: bold;
    margin: 10px 0;
    span {
      -webkit-box-decoration-break: clone;
      background: linear-gradient(
        0deg,
        rgba(255, 0, 255, 0),
        rgba(255, 0, 255, 0) 16%,
        rgb(241, 210, 42) 0px,
        rgb(241, 210, 42) 32%,
        rgba(255, 0, 255, 0) 0px
      );
      padding: 0px 0.1em 0px 0px;
    }
  }

  &_wrap {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin: auto;
    width: 90%;
  }
  &_item {
    position: relative;
    margin: 0 auto;
    cursor: pointer;

    img {
      height: 150px;
      width: 100%;
      object-fit: contain;
    }
    p {
      color: white;
      background: var(--green);
      padding: 5px 10px;
      opacity: 0.9;
      display: flex;
      justify-content: center;
      align-items: center;
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      font-size: 0.7rem;
    }
    section {
      position: absolute;
      display: flex;
      margin-top: -10px;
      align-items: baseline;
      justify-content: center;
      span {
        margin: 0 10px;
      }
      h6 {
        color: var(--text);
      }
      .ratings {
        display: flex;
      }
      .reviews {
        display: flex;
      }
    }
  }

  .link {
    margin: 20px auto;
    width: 70%;
    display: flex;
    justify-content: flex-end;
    a {
      background: var(--green);
      color: white;
      padding: 5px 10px;
      border-radius: 8px;
    }
  }

  @media only screen and (min-width: 700px) {
    h1 {
      font-size: 1.3rem;
      margin-bottom: 20px;
    }
    &_wrap {
      grid-template-columns: 1fr 1fr 1fr;
      gap: 20px;
      row-gap: 25px;
    }
    &_item {
      section {
        margin-top: -4px;
      }
    }
    .link {
      margin: 35px auto;
      width: 90%;
    }
  }

  @media only screen and (min-width: 1000px) {
    h1 {
      font-size: 1.5rem;
      margin-bottom: 30px;
    }
    &_wrap {
      width: 80%;
      row-gap: 30px;
    }
    &_item {
      section {
        margin-top: 1px;
        margin-left: 20px;
      }
    }
    .link {
      width: 80%;
    }
  }

  @media only screen and (min-width: 1200px) {
    h1 {
      font-size: 1.7rem;
      margin: 40px 0;
    }
    &_item {
      img {
        height: 180px;
        object-fit: cover;
      }
      p {
        font-size: 1.2rem;
        border-radius: 6px;
      }
    }

    .link {
      width: 70%;
      justify-content: center;
      a {
        padding: 10px 18px;
        font-size: 1.05rem;
      }
    }
  }

  @media only screen and (min-width: 1800px) {
    &_wrap {
      width: 60%;
    }
  }
}
</style>