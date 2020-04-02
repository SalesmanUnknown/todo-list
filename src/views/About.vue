<template>
  <div class="about">
    <h1>About us</h1>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit.
      <br />Nam harum, adipisci nihil quam blanditiis minus,
      <br />vel quia cum expedita aliquid consectetur?
      <br />Vel error nemo quo alias?
      <br />Ab natus quisquam totam.
    </p>
    <button>
      <router-link to="/list">Get started</router-link>
    </button>
  </div>
</template>


<style lang="scss">
.about {
  min-height: 90vh;
  background-image: url("../assets/second.jpg");
  background-size: cover;
  background-position-y: 55%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  text-shadow: 2px 2px rgb(25, 32, 34);
}

.about h1 {
  padding-bottom: 20px;
  font-family: sans-serif;
  font-size: 50px;
}

.about p {
  padding-bottom: 20px;
  font-family: sans-serif;
  font-size: 18px;
}

.about button {
  border: none;
  margin-top: 10px;
  width: 120px;
  height: 40px;
  background-color: white;
  color: rgb(25, 32, 34);
  font-family: sans-serif;
  cursor: pointer;
  transition: 0.3s ease;
}

.about button:hover {
  opacity: 0.9;
}

.about a {
  text-decoration: none;
  color: currentColor;
}
</style>