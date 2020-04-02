<template>
  <div id="app">
    <Header />
    <router-view :items="todo" @addList="addList" @deleteList="deleteList" />
  </div>
</template>

<script>
import Header from "@/components/header.vue";
import axios from "axios";
export default {
  components: {
    Header
  },
  data() {
    return {
      todo: []
    };
  },
  methods: {
    async getItems() {
      try {
        let result = await axios.get("http://localhost:3000/items");
        this.todo = result.data;
      } catch (error) {
        console.log(error);
      }
    },
    async addList(newProduct) {
      try {
        await axios.post("http://localhost:3000/items", newProduct);
        this.getItems();
      } catch (error) {
        console.log(error);
      }
    },
    async deleteList(id) {
      try {
        await axios.delete(`http://localhost:3000/items/${id}`, id);
        this.getItems();
      } catch (error) {
        console.log(error);
      }
    }
  },
  mounted() {
    this.getItems();
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
