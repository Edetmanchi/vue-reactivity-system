
<template>
  <div class="container">
    <div class="logo-container">
      <span class="logo">Learning</span>
    </div>
    <div>
      <h1 v-if="userName">Hello, {{ userName }}!</h1>
      <h1 v-else>Welcome!</h1>
    </div>
    <div>
      <!-- <button type="button" class="button">Get started</button> -->
    </div>
  </div>
</template>

<script setup>
defineProps({
  userName: {
    type: String,
    default: "",
  },
});
</script>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  margin: 0px 10px;
  padding: 4px;
  border-bottom: rgb(113 113 122) 1px solid;
}

.logo {
  align-self: center;
  font: 200;
  font-weight: bold;
  font-size: 20px;
}
</style>