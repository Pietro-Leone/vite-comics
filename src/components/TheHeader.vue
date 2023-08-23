<script>
export default {
  data() {
    return {
      menu: [
        { title: "Character" },
        { title: "Comics" },
        { title: "Movies" },
        { title: "Tv" },
        { title: "Games" },
        { title: "Collectibles" },
        { title: "Videos" },
        { title: "Fans" },
        { title: "News" },
        { title: "Shop" }
      ],
    }
  }
}
</script>

<template>
  <header>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
      <div class="container">
        <a class="navbar-brand" href="#"><img src="../assets/img/dc-logo.png" alt="logo" style="width: 80px;"></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup"
          aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end h-100" id="navbarNavAltMarkup">
          <div class="navbar-nav text-uppercase">
            <a class="nav-link" href="#" v-for="el in menu">
              {{ el.title }}
              <div class="after-div" tabindex="0"></div>
            </a>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.nav-link {
  font-weight: bolder;
  position: relative;
  text-align: center;

  &:hover {
    color: $color-primary;
  }

  .after-div {
    position: absolute;
    left: 0;
    bottom: -33px;
    display: flex;
    justify-content: center;
    align-items: end;
    width: 100%;
    height: 100px;

    &:focus::after {
      content: "";
      width: 80%;
      height: 5px;

      background-color: $color-primary;
    }
  }
}
</style>