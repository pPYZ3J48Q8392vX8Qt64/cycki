<template>
  <div class="header-container">
    <header class="the-header">
      <div class="logo">
        <nuxt-link to="/" class='header-text'>POWERBANKS</nuxt-link>
      </div>
      <TheSideNavToggle @toggle="$emit('sidenavToggle')" />
      <div class="navigation-items">
        <ul class="nav-list">
          <li class="nav-item">
            <nuxt-link to="/posts">Powerbanks</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/about">Chargers</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/about">Solar Charger</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/about">Power Wiki</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/admin">About</nuxt-link>
          </li>
        </ul>
      </div>
    </header>
  </div>
</template>

<script>
import TheSideNavToggle from "@/components/Navigation/TheSideNavToggle";

export default {
  name: "TheHeader",
  components: {
    TheSideNavToggle,
  },
};
</script>


<style scoped>
.header-container {
  height: 60px;
}

.header-text{
  color: #FF761E;
}

.the-header {
  display: flex;
  width: 100%;
  position: fixed;
  height: 80px;
  justify-content: space-between;
  align-items: center;
  background-color: #FDFEFE;
  z-index: 100;
  box-sizing: border-box;
  padding: 0 30px;
}

.logo {
  margin: 0 10px;
  font-size: 1.3rem;
}

.logo a {
  text-decoration: none;
  color: #000000;
}

.navigation-items {
  display: none;
}

@media (min-width: 768px) {
  .navigation-items {
    display: block;
  }
}

.nav-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
}

.nav-item {
  margin: 0 10px;
}

.nav-item a {
  text-decoration: none;
  color: #000000;
  font-size: 18px;
}

.nav-item a:hover,
.nav-item a:active,
.nav-item a.nuxt-link-active {
  color: red;
}
</style>
