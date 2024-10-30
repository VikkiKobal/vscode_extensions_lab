<template>
  <div class="container">
    <div class="logo">
      <img :src="extesionImg" alt="icon" class="icon-img" />
    </div>
    <h2 class="extension-title">{{ extesionTitle }}</h2>
    <p class="extension-description">{{ extesionDescription }}</p>
    <img
      class="settings"
      src="https://cdn-icons-png.flaticon.com/512/5166/5166607.png"
    />
  </div>
</template>

<script>
export default {
  name: "OneExtension",
  props: {
    extesionTitle: {
      type: String,
      required: true,
    },
    extesionImg: {
      type: String,
      required: true,
    },
    extesionDescription: {
      type: String,
      required: true,
    },
  },
};
</script>
<style>
.container {
  display: flex;
  align-items: center;
  padding: 10px;
  border-radius: 4px;
  background-color: #474444;
}

.icon-img {
  width: 50px;
  height: 50px;
}

.extension-title {
  font-size: 16px;
  font-weight: bold;
  color: #f9fcff;
}

.extension-description {
  font-size: 14px;
  color: #ffe9e9;
  margin: 5px;
}

.settings {
  width: 20px;
  height: 20px;
  margin-left: auto;
}
</style>
