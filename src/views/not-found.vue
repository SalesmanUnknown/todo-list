<template>
  <div class="found">
    <h1>Not-found</h1>
    <p>Something went wrong...</p>
    <button>
      <router-link to="/">Home</router-link>
    </button>
  </div>
</template>

<script>
export default {};
</script>

<style>
.found {
  min-height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.found h1 {
  font-family: sans-serif;
  font-size: 50px;
  padding-bottom: 5px;
}

.found p {
  font-family: sans-serif;
  font-size: 20px;
  padding-bottom: 7px;
}
.found button {
  border: none;
  background-color: rgb(25, 32, 34);
  width: 100px;
  height: 35px;
  color: white;
  font-family: sans-serif;
  transition: 0.3s ease;
  cursor: pointer;
}

.found a {
  text-decoration: none;
  color: currentColor;
}

.found button:hover {
  opacity: 0.8;
}
</style>