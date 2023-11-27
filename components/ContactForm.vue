<!-- components/ContactForm.vue -->

<template>
    <form @submit.prevent="submitForm">
      <label for="name">Name:</label>
      <input type="text" id="name" v-model="formData.name" required />
  
      <label for="email">Email:</label>
      <input type="email" id="email" v-model="formData.email" required />
  
      <label for="message">Message:</label>
      <textarea id="message" v-model="formData.message" required></textarea>
  
      <button type="submit">Submit</button>
    </form>
  </template>
  
  <script>
  export default {
    data() {
      return {
        formData: {
          name: '',
          email: '',
          message: '',
        },
      };
    },
    methods: {
      submitForm() {
        // Handle form submission logic here
        console.log('Form submitted:', this.formData);
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add your component-specific styles here */
  </style>
  