<template>
  <header>
    <div>
      <b-button v-b-toggle.sidebar-backdrop>Toggle Sidebar</b-button>

      <b-sidebar
        no-header
        id="sidebar-backdrop"
        title="Reviewly"
        :backdrop-variant="variant"
        backdrop
        shadow
      >
        <div class="px-3 py-2">hello world</div>
      </b-sidebar>
    </div>
    <div class="header-wrap">
      <div class="logo"><router-link to="/">Reviewly</router-link></div>
      <nav>
        <router-link to="/">Login</router-link> |
        <router-link to="/about">About</router-link>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      variant: "dark",
    };
  },
};
</script>

<style lang="scss" scoped>
header {
  padding: 20px;
  background: var(--primary);
}
.logo {
  a {
    color: white;
  }
}
.header-wrap {
  display: flex;
  justify-content: space-between;
  color: white;
  margin: auto;
  width: 90%;
  nav {
    a {
      color: white;
    }
  }
}
</style>
