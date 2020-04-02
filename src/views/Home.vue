<template>
  <div class="home">
    <h1 class="hpage">Homepage</h1>
    <div class="para">
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
        <br />Cum quae debitis tenetur exercitationem nobis tempore rerum
        assumenda dolores consequatur. <br />Odit error ex delectus voluptatem
        sit doloremque eveniet magnam maxime magni.
        <br />
      </p>
    </div>
    <button>
      <router-link to="/about">Learn more</router-link>
    </button>
  </div>
</template>

<script>
import { gsap } from "gsap";
// @ is an alias to /src
export default {
  name: "Home",
  mounted() {
    gsap.fromTo(".hpage", 1, { opacity: 0, y: "-30" }, { opacity: 1, y: 0 });
  }
};
</script>

<style lang="scss">
.home {
  background-image: url("../assets/unsplash.jpg");
  background-size: cover;
  background-position: center;
  min-height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  text-shadow: 2px 2px rgb(25, 32, 34);
}

.home h1 {
  font-family: sans-serif;
  font-size: 50px;
  padding-bottom: 20px;
}

.home p {
  font-family: sans-serif;
  font-size: 18px;
}

.home button {
  border: none;
  margin-top: 10px;
  width: 120px;
  height: 40px;
  background-color: rgb(25, 32, 34);
  color: white;
  font-family: sans-serif;
  cursor: pointer;
  transition: 0.3s ease;
}

.home button:hover {
  opacity: 0.9;
}

.home a {
  text-decoration: none;
  color: currentColor;
}
</style>
