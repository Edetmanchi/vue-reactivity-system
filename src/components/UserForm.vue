<template>
  <div class="container">
    <form @submit.prevent="submitForm">
      <div>
        <div>
          <h5 class="title">Let's Know you</h5>
        </div>
        <p class="description">Enter Informations to get Started</p>
      </div>
      <div class="form-group">
        <label class="label" for="name">Name:</label>
        <input class="input" type="text" id="name" v-model="name" required />
      </div>
      <div class="form-group">
        <label class="label" for="email">Email:</label>
        <input class="input" type="email" id="email" v-model="email" required />
      </div>
      <div class="form-group">
        <label class="label" for="age">Age:</label>
        <input class="input" type="number" id="age" v-model="age" required />
      </div>
      <button type="submit" class="submit-button">Send</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from "vue";

const name = ref("");
const email = ref("");
const age = ref(null);

const emit = defineEmits(["form-submitted"]);

const submitForm = () => {
  emit("form-submitted", {
    name: name.value,
    email: email.value,
    age: age.value,
  });

  name.value = "";
  email.value = "";
  age.value = null;
};
</script>

<style scoped>
.container {
  max-width: 45em;
  margin: 20px auto;
  align-items: center;
  justify-content: center;
  border: rgb(209 213 219) 1px solid;
  padding: 20px 15px;
}
.form-group {
  margin-bottom: 25px;
  padding: 0px 10px;
}

.title {
  margin-bottom: 5px;
  font-size: 30px;
  font-weight: bold;
  color: rgb(55 65 81);
}
.description {
  margin-bottom: 3px;
  color: (55 65 81);
  text-align: center;
  font-size: 18px;
}
.label {
  display: block;
  margin-bottom: 6px;
  font-size: 27px;
}
.input {
  background-color: rgb(209 213 219);
  border: rgb(156 163 175) solid 1px;
  color: rgb(17 24 39);
  font-size: 15px;
  align-items: center;
  border-radius: 8px;
  display: block;
  width: 95%;
  padding: 12px;
}
.submit-button {
  color: white;
  padding: 10px 35px;
  font-size: 20px;
  border-radius: 10px;
  background-color: rgb(59 130 246);
}
</style>


























































<template>
  <div class="container">
    <form @submit.prevent="submitForm">
      <div>
        <div>
          <h5 class="title">Let's Know you</h5>
        </div>
        <p class="description">Enter Informations to get Started</p>
      </div>
      <div class="form-group">
        <label class="label" for="name">Name:</label>
        <input class="input" type="text" id="name" v-model="name" required />
      </div>
      <div class="form-group">
        <label class="label" for="email">Email:</label>
        <input class="input" type="email" id="email" v-model="email" required />
      </div>
      <div class="form-group">
        <label class="label" for="age">Age:</label>
        <input class="input" type="number" id="age" v-model="age" required />
      </div>
      <button type="submit" class="submit-button">Send</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from "vue";

const name = ref("");
const email = ref("");
const age = ref(null);

const emit = defineEmits(["form-submitted"]);

const submitForm = () => {
  emit("form-submitted", {
    name: name.value,
    email: email.value,
    age: age.value,
  });

  name.value = "";
  email.value = "";
  age.value = null;
};
</script>

<style scoped>
.container {
  max-width: 45em;
  margin: 20px auto;
  align-items: center;
  justify-content: center;
  border: rgb(209 213 219) 1px solid;
  padding: 20px 15px;
}
.form-group {
  margin-bottom: 25px;
  padding: 0px 10px;
}

.title {
  margin-bottom: 5px;
  font-size: 30px;
  font-weight: bold;
  color: rgb(55 65 81);
}
.description {
  margin-bottom: 3px;
  color: (55 65 81);
  text-align: center;
  font-size: 18px;
}
.label {
  display: block;
  margin-bottom: 6px;
  font-size: 27px;
}
.input {
  background-color: rgb(209 213 219);
  border: rgb(156 163 175) solid 1px;
  color: rgb(17 24 39);
  font-size: 15px;
  align-items: center;
  border-radius: 8px;
  display: block;
  width: 95%;
  padding: 12px;
}
.submit-button {
  color: white;
  padding: 10px 35px;
  font-size: 20px;
  border-radius: 10px;
  background-color: rgb(59 130 246);
}
</style>