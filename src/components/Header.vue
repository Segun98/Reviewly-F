<template>
  <header>
    <div class="header-wrap">
      <div class="mobile">
        <!-- open drawer menu icon  -->
        <img
          :src="Menu"
          role="button"
          alt="menu"
          aria-label="menu"
          aria-roledescription="menu"
          class="drawer"
          v-b-toggle.sidebar-backdrop
        />

        <!-- bootstrap drawer  -->
        <b-sidebar
          no-header
          id="sidebar-backdrop"
          title="Reviewly"
          :backdrop-variant="variant"
          backdrop
          shadow
        >
          <div class="drawer_content">
            <section class="drawer_header">
              <img :src="Logo" alt="logo" />
              Reviewly
            </section>

            <section class="drawer_body">
              <ul>
                <li>Login</li>
                <li>Signup</li>
                <li>Top Apartments</li>
                <li>Add an apartment</li>
                <li>Contact us</li>
              </ul>
            </section>
          </div>
        </b-sidebar>

        <!-- end of bootstrap drawer  -->

        <div class="logo">
          <router-link to="/">
            <img :src="Logo" alt="logo" />Reviewly</router-link
          >
        </div>
      </div>

      <nav v-if="!isLoggedIn" class="right-nav">
        <router-link to="/">Login</router-link> |
        <router-link to="/about">Signup</router-link>
      </nav>
      <nav v-else class="right-nav">
        <b-button class="contact-btn">Contact Us</b-button>
      </nav>
    </div>
  </header>
</template>

<script>
import Logo from "@/assets/svgs/pentagon-bottom-right.svg";
import Menu from "@/assets/svgs/menu.svg";
export default {
  name: "Header",
  data() {
    return {
      variant: "dark",
      Logo,
      Menu,
      isLoggedIn: true,
    };
  },
};
</script>

<style lang="scss" scoped>
header {
  padding: 20px;
  background: white;
}

.logo {
  a {
    color: var(--green);
  }
}
.header-wrap {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: var(--green);
  margin: auto;

  .mobile {
    display: flex;
  }

  .drawer {
    display: inline;
    margin-right: 10px;
    height: 30px;
    width: 30px;

    &_content {
      margin: auto;
      width: 90%;
    }
    &_header {
      color: var(--green);
      font-size: 1.4rem;
      margin: 20px 0;
      padding-bottom: 5px;
      border-bottom: 0.5px solid var(--text);
    }
  }

  .logo {
    font-size: 1.4rem;
  }

  nav {
    .contact-btn {
      background: var(--green);
      border: none;
      border-radius: 7px;
    }
    a {
      color: var(--green);
    }
  }

  @media only screen and (min-width: 700px) {
    width: 90%;
    .drawer {
      display: none;
    }
  }

  @media only screen and (min-width: 1800px) {
    width: 60%;
    .logo {
      font-size: 1.8rem;
    }
  }
}
</style>
