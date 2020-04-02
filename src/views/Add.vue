<template>
  <div>
    <form>
      <p>Add an item to the database!</p>
      <label>Item</label>
      <input type="text" v-model="item" />
      <label class="move">Urgency</label>
      <input type="text" v-model="urgency" />
      <button @click="addList">Add</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      item: "",
      urgency: ""
    };
  },
  methods: {
    addList(event) {
      event.preventDefault();

      this.$emit("addList", {
        item: this.item,
        urgency: this.urgency,
        done: "false"
      });

      this.item = "";
      this.urgency = "";
    }
  }
};
</script>

<style>
form {
  min-height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-size: 24px;
  font-family: sans-serif;
  background-color: rgb(243, 242, 242);
}

form .move {
  padding-top: 20px;
}

form input {
  width: 250px;
  height: 30px;
}

form button {
  margin-top: 15px;
  width: 120px;
  height: 40px;
  border: none;
  background-color: rgb(25, 32, 34);
  color: white;
  cursor: pointer;
  transition: 0.3s ease;
}

form button:hover {
  opacity: 0.9;
}

form p {
  padding-bottom: 20px;
  font-size: 35px;
}
</style>