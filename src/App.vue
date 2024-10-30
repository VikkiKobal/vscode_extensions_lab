<template>
  <div>
    <input
      type="text"
      v-model="searchExtension"
      placeholder="Введіть назву розширення"
    />
    <extension-list :listOfExtensions="filteredExtensions" />
  </div>
</template>

<script>
import ExtensionList from "./components/ExtensionList.vue";

export default {
  name: "App",
  components: {
    ExtensionList,
  },
  data() {
    return {
      searchExtension: "",
      extensions: [
        {
          id: 1,
          title: "Git Graph",
          imgSrc:
            "https://mhutchie.gallerycdn.vsassets.io/extensions/mhutchie/git-graph/1.30.0/1617594001998/Microsoft.VisualStudio.Services.Icons.Default",
          description:
            "View a Git Graph of your repository, and perform Git actions from the graph.",
        },
        {
          id: 2,
          title: "Git History",
          imgSrc:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTCEj_V6_aIHeHJk9LAEq1kk5Bs7bjAzb82qw&s",
          description:
            "View git log, file history, compare branches or commits",
        },
        {
          id: 3,
          title: "Live Server",
          imgSrc:
            "https://ritwickdey.gallerycdn.vsassets.io/extensions/ritwickdey/liveserver/5.7.9/1661914858952/Microsoft.VisualStudio.Services.Icons.Default",
          description:
            "Launch a development local Server with live reload feature for static & dynamic pages",
        },
        {
          id: 4,
          title: "Vetur",
          imgSrc:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQT9QTtPSR9q3aiUhivscMjVoys6vPfU94PuEKXkXO5eYC4DyZaMiPtWuRaVHBfc7XB0EM&usqp=CAU",
          description: "Vue tooling for VS Codes",
        },
        {
          id: 5,
          title: "Vue VSCode Snippets",
          imgSrc:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQT9QTtPSR9q3aiUhivscMjVoys6vPfU94PuEKXkXO5eYC4DyZaMiPtWuRaVHBfc7XB0EM&usqp=CAU",
          description: "Snippets that will supercharge your Vue workflow",
        },
      ],
    };
  },
  computed: {
    filteredExtensions() {
      return this.extensions.filter((extension) =>
        extension.title
          .toLowerCase()
          .includes(this.searchExtension.toLowerCase())
      );
    },
  },
};
</script>

<style>
</style>
