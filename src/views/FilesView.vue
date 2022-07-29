<template>
  <div class="files">
    <h4>{{ path }}</h4>
    <div class="list" v-for="content in folderContent" v-bind:key="content">
      <span>{{ content }}</span>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "FilesView",
  props: {},
  data() {
    return {
      folderContent: [],
      path: "",
    };
  },
  mounted() {
    console.log("hehe");
    axios.get("http://localhost:3000/api/files").then((res) => {
      console.log(res);
      this.folderContent = res.data.content;
    });

    axios.get("http://localhost:3000/api/files/location").then((res) => {
      console.log(res);
      this.path = res.data.path;
    });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
