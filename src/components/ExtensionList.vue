<template>
  <div class="extension-list">
    <one-extension
      v-for="extension in listOfExtensions"
      :key="extension.id"
      :iconLink="extension.link"
      :extesionImg="extension.imgSrc"
      :extesionTitle="extension.title"
      :extesionDescription="extension.description"
    />
  </div>
</template>

<script>
import OneExtension from "./OneExtension.vue";

export default {
  name: "ExtensionList",
  components: {
    OneExtension,
  },
  props: {
    listOfExtensions: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style>
.extension-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 20px;
  background-color: #474444;
}
</style>
