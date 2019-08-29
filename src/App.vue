<template>
  <div id="app">
    <main class="container">
      <search :keyWord="keyWord"></search>
      <section class="category">
        <h2>Products Category</h2>
        <p>Find your questions/knowledge based on the categories</p>
        <div class="category-wrap">
          <category
            v-for="(item, index) in filterCategory"
            :key="index"
            :url="item.url"
            :desc="item.desc"
          ></category>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
import Category from "./components/Category.vue";
import Search from "./components/Search.vue";
export default {
  name: "App",
  components: {
    Category,
    Search
  },
  data() {
    return {
      keyWord: '',
      categories: [
        {
          desc: "General Discussion",
          url: require("./assets/img/general.png")
        },
        {
          desc: "Power Tools",
          url: require("./assets/img/power-tool.png")
        },
        {
          desc: "Dust Management and Vacuum Cleaners",
          url: require("./assets/img/dust-management.png")
        },
        {
          desc: "Tools Inserts",
          url: require("./assets/img/tool-insert.png")
        },
        {
          desc: "Direct Fastening",
          url: require("./assets/img/direct-fastening.png")
        },
        {
          desc: "Measuring Tools and Scanners",
          url: require("./assets/img/measuring-tool.png")
        },
        {
          desc: "Fastener",
          url: require("./assets/img/fasteners.png")
        },
        {
          desc: "Firestop and Fire Protection",
          url: require("./assets/img/fire-stop.png")
        },
        {
          desc: "Installation System",
          url: require("./assets/img/installation-system.png")
        },
        {
          desc: "Construction Chemicals",
          url: require("./assets/img/construction-chemicals.png")
        },
        {
          desc: "Software",
          url: require("./assets/img/software.png")
        },
        {
          desc: "Other",
          url: require("./assets/img/other.png")
        }
      ]
    };
  },
  computed: {
    filterCategory() {
      return this.categories.filter(x => x.desc.toLowerCase().match(this.keyWord.toLowerCase()))
    }
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
body {
  font-family: "Hilti Bold", Arial, Helvetica, sans-serif;
}

.container {
  max-width: 1000px;
  width: 100%;
  margin: 0 auto;
}

</style>
