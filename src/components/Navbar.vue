<template>
  <div class="nav-wrapper">
    <a data-target="mobile-demo" class="sidenav-trigger"
      ><i class="material-icons">menu</i></a
    >
    <ul class="left">
      <li>
        <router-link
          exact
          active-class="active"
          to="/"
          class="brand-logo left show-on-medium-and-up"
          >Profiler</router-link
        >
      </li>
    </ul>
    <ul id="nav-mobile" class="left hide-on-med-and-down">
      <li>
        <router-link active-class="active" to="/users"
          >Пользователи</router-link
        >
      </li>
      <li>
        <router-link active-class="active" to="/articles">Статьи</router-link>
      </li>
      <li>
        <router-link active-class="active" to="/repositories"
          >Репозитории</router-link
        >
      </li>
    </ul>
    <NavDropdown />
  </div>
</template>

<script>
import NavDropdown from "./NavDropdown";
export default {
  name: "Navbar",
  components: { NavDropdown }
};
</script>

<style scoped lang="sass">
.sidenav-trigger
  margin: 0 5px
.brand-logo
  position: static !important
  padding: 0 5px !important
img.right
  width: 22px
li > a
  padding: 0 10px !important
</style>
