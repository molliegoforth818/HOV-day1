<template>
  <div id="app">
    <h1>Hello Frontend Devs</h1>
    <h2>What is your favorite JS framework?</h2>
    <button @click="selectFramework('Angular')">Angular</button>
    <button @click="selectFramework('Vue')">Vue</button>
    <button @click="selectFramework('React')">React</button>
    <div v-if="frameworkSelection !== null">
      <p>Good choice! {{ frameworkSelection }} is a great tool!</p>
      <div v-if="frameworkImg !== null">
        <img :src="frameworkImg" :alt="frameworkSelection" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      frameworkSelection: null,
      frameworkImg: null,
    };
  },
  methods: {
    selectFramework(frameworkName) {
      this.frameworkSelection = frameworkName;
      if (frameworkName === "Angular") {
        this.frameworkImg =
          "http://assets.stickpng.com/images/5847ea22cef1014c0b5e4833.png";
      } else if (frameworkName === "Vue") {
        this.frameworkImg =
          "https://3lhowb48prep40031529g5yj-wpengine.netdna-ssl.com/wp-content/uploads/2019/10/logo-vuejs-min.png";
      } else if (frameworkName === "React") {
        this.frameworkImg =
          "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS522cvfykAGpHa9VldhoyaVHuQY6PtojUdnw&usqp=CAU";
      }
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
