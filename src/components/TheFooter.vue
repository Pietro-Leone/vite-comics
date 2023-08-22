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
        <div class="credits d-flex p-4">
          <div v-for="credit in credits" class="px-3">
            <h5 class="text-uppercase">{{ credit.title }}</h5>
            <ul class="list-unstyled py-2">
              <li v-for="element in credit.elements">
                <a href="#">{{ element }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="dc-bg position-absolute"></div>
      </div>
    </div>

    <div class="contacts-container">
      <div class="container">

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
  height: 450px;
}

.credits {
  flex-direction: column;
  flex-wrap: wrap;
  height: 450px;

  h5 {
    font-weight: bold;
    font-size: 1.5rem;
  }
}

.dc-bg {
  background-image: url("../assets/img/dc-logo-bg.png");
  background-position: center;
  background-repeat: no-repeat;
  height: 450px;
  width: 600px;
  right: 0;
}

a,
h5 {
  color: white;
  text-decoration: none;
}
</style>