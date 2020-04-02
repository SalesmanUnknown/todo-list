<template>
  <div class="list">
    <div class="box" v-for="todos in items" :key="todos.id">
      <h1>{{ todos.item }}</h1>
      <p>Hitnost: {{ todos.urgency }}</p>
      <p>Zavrseno: {{ todos.done == "true" ? "Uradjeno" : "Nije" }}</p>
      <div class="buttons">
        <button @click="deleteList(todos.id)" class="butt">
          <i class="fas fa-trash"></i>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["items"],
  created() {
    console.log(this.props);
  },
  methods: {
    deleteList(id) {
      this.$emit("deleteList", id);
    }
  }
};
</script>

<style lang="scss">
.list {
  min-height: 90vh;
  display: flex;
  flex-wrap: wrap;
  padding-top: 50px;
  justify-content: center;
  background-color: rgb(243, 242, 242);
}

.box {
  width: 300px;
  height: 200px;
  background-color: rgb(25, 32, 34);
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin-right: 20px;
  font-family: sans-serif;
  color: white;
}

.buttons button {
  width: 40px;
  height: 40px;
  border: none;
  border-radius: 20px;
  outline: none;
  transition: 0.3s ease;
  cursor: pointer;
  background-color: rgb(224, 72, 72);
}

.buttons button:hover {
  opacity: 0.9;
}

.butt2 {
  background-color: rgb(79, 241, 79);
}
.box h1 {
  padding-bottom: 10px;
  font-size: 20px;
}

.box p {
  padding-bottom: 20px;
}
</style>
