 <template>
    <CardLayout>
      <h3>{{ user.name }}</h3>
      <p>Email: {{ user.email }}</p>
      <p>Age: {{ user.age }}</p>
    </CardLayout>
  </template>
  
  <script setup>
  defineProps({
    user: {
      type: Object,
      required: true,
    },
  });
  </script>
  
  <style scoped>
  h3 {
    margin-bottom: 10px;
  }
  
  p {
    margin: 5px 0;
  }
  </style>