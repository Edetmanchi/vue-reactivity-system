
<template>
  <div class="">
    <Header :userName="userName" />

    <main>
      <UserForm v-if="showForm" @form-submitted="handleFormSubmit" />

      <div class="cards-container">
        <UserCard v-for="(user, index) in users" :key="index" :user="user" />
      </div>
    </main>
  </div>
</template>

<script setup>
import {ref} from "vue";
import Header from "./components/Header.vue";
import UserForm from "./components/UserForm.vue";
import UserCard from "./components/UserCard.vue";

const userName = ref("");
const users = ref([]);
const showForm = ref(true);

const handleFormSubmit = (formData) => {
  userName.value = formData.name; 
  users.value.push(formData); 
  showForm.value = false;
};
</script>

<style>
.cards-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
</style>