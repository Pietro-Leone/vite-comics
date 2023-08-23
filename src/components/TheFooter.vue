<script>
export default {
  data() {
    return {
      credits: [
        {
          title: "Dc Comics",
          elements: [
            "characters",
            "comics",
            "movies",
            "tv",
            "games",
            "videos",
            "news"
          ],
        }, {
          title: "Shop",
          elements: [
            "shop dc",
            "shop dc collectibles"
          ],
        }, {
          title: "DC",
          elements: [
            "terms of use",
            "privacy policy (new)",
            "ad choices",
            "advertising",
            "jobs",
            "subscription",
            "talent workshop",
            "cpsc certificates",
            "ratings",
            "shop help",
            "contact us"
          ],
        }, {
          title: "Sites",
          elements: [
            "dc",
            "mad magazine",
            "dc kids",
            "dc universe",
            "dc power visa"
          ],
        }
      ]
    };
  },
}
</script>

<template>
  <footer>

    <div class="credits-container">
      <div class="container d-flex justify-content-between position-relative">
        <div class="credits d-flex py-4">
          <div v-for="credit in credits" class="pe-4">
            <h5 class="text-uppercase">{{ credit.title }}</h5>
            <ul class="list-unstyled m-0 py-2">
              <li v-for="element in credit.elements">
                <a href="#" class="text-capitalize">{{ element }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="dc-bg position-absolute"></div>
      </div>
    </div>

    <div class="contacts-container">
      <div class="container">
        <div class="d-flex justify-content-between">
          <button type="button" class="btn btn-outline-primary text-uppercase">sign-up now!</button>
          <div class="d-flex align-items-center">
            <h4>Follow US</h4>
            <img src="../assets/img/footer-facebook.png" alt="icon">
            <img src="../assets/img/footer-twitter.png" alt="icon">
            <img src="../assets/img/footer-youtube.png" alt="icon">
            <img src="../assets/img/footer-pinterest.png" alt="icon">
            <img src="../assets/img/footer-periscope.png" alt="icon">
          </div>
        </div>
      </div>
    </div>

  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.credits-container {
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}

.credits {
  flex-direction: column;
  flex-wrap: wrap;
  height: 380px;

  h5 {
    font-weight: bold;
    font-size: 1.5rem;
  }
}

.contacts-container {
  background-color: $color-secondary;
  padding: 2rem 0;

  button {
    color: white;
    border-radius: 0;
  }

  h4 {
    color: $color-primary;
    text-transform: uppercase;
    margin: 0;
    width: 100%;
  }

  img {
    margin: 0 .5rem;
    width: 40px;
  }
}

.dc-bg {
  background-image: url("../assets/img/dc-logo-bg.png");
  background-position: center;
  background-repeat: no-repeat;
  height: 380px;
  width: 600px;
  right: 0;
}

a,
h5 {
  color: white;
  text-decoration: none;
}
</style>