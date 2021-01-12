<template>
  <section class="location" v-if="lcdas.length > 0">
    <h1>Apartment Reviews in <span> Top Places </span></h1>
    <div class="location_wrap">
      <div v-for="l in lcdas" :key="l.id" class="location_item">
        <img :src="l.image" />
        <p>{{ l.LCDA }}</p>
      </div>
    </div>
    <div class="link">
      <router-link to="/about">More places</router-link>
    </div>
  </section>
</template>

<script>
// import lcdas from "@/lcda.js";
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
          name: "John's Space",
          LCDA: "Eti-Osa",
          image: require("@/assets/header3.jpg"),
        },
        {
          id: 4,
          name: "John's Space",
          LCDA: "Lekki",
          image: require("../assets/header1.jpg"),
        },
        {
          id: 5,
          name: "John's Space",
          LCDA: "Ifako-Ijaiye",
          image: require("../assets/header23.jpg"),
        },
        {
          id: 6,
          name: "John's Space",
          LCDA: "Epe",
          image: require("../assets/header3.jpg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.location {
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
      font-size: 0.9rem;
    }
  }

  .link {
    margin: 10px auto;
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
    }
    .link {
      margin: 15px auto;
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
    &_wrap {
      gap: 15px;
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