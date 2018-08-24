<template>
  <div id="app" class="container-fluid">
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-light py-3">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img src="./assets/images/logo-full.svg" height="28" />
        </a>

        <ul class="nav">
          <li class="nav-item">
            <a class="nav-link" href="#"><img height="24" width="24" src="https://unpkg.com/simple-icons@latest/icons/github.svg" /></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><img height="24" width="24" src="https://unpkg.com/simple-icons@latest/icons/telegram.svg" /></a>
          </li>
        </ul>
      </div>
    </nav>

    <router-view/>

    <!-- Footer -->
    <footer class="d-flex flex-column justify-content-center align-items-center">
      <p class="contact">
        Please feel free to contact us at <a href="mailto:contact@exeum.org">contact@exeum.org</a>
      </p>
      <p class="align-bottom copyright">
        © 2018 Exeum Foundation
      </p>
    </footer>
  </div>
</template>

<style lang="scss" scoped>
@import "./scss/res.scss";
#app {
  @extend %body1;
  padding: 0rem;
  margin: 0rem;
  color: $text-default;
  background-color: $bg-color-default;
}

nav {
  // background-color: $bg-navigation;
}

nav > div {
  max-width: $max-contents-width;
}

footer {
  height: $footer-height;
  color: white;
  background-color: $bg-footer;
}

.contact {
  @extend %body1;
  padding-top: 1.5rem;
}

.copyright {
  @extend %body2;
}
</style>
