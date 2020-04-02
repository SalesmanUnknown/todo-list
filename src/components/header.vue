<template>
  <div>
    <div class="header">
      <div class="logo">
        <router-link to="/">
          <h1>ToDo List</h1>
        </router-link>
      </div>
      <ul class="nav-links">
        <li>
          <router-link class="nav-link" to="/about">About</router-link>
        </li>
        <li>
          <router-link class="nav-link" to="/list">List</router-link>
        </li>
        <li>
          <router-link class="nav-link" to="/add">Add to list</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "hedr"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header {
  min-height: 10vh;
  background-color: rgb(25, 32, 34);
  display: flex;
  align-content: center;
  justify-content: space-between;
}

.header .logo {
  flex: 1;
  align-self: center;
  font-family: sans-serif;
  font-size: 19px;
  color: white;
  transition: 0.5s ease;
  padding-left: 50px;
}

.header .logo:hover {
  opacity: 0.8;
}

.header ul {
  display: flex;
  flex: 1;
  list-style: none;
  align-self: center;
  padding-left: 600px;
}

.header li {
  display: flex;
  flex: 0.5;
  align-content: center;
  font-size: 18px;
  font-family: sans-serif;
  color: white;
}

.header .nav-link {
  text-decoration: none;
  color: currentColor;
  transition: 1s ease;
}

a {
  text-decoration: none;
  color: currentColor;
}

.nav-link:hover {
  opacity: 0.8;
}
</style>
