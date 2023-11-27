<!-- pages/contact.vue -->

<template>
    <div>
      <h1>Contact Page</h1>
      <ContactForm />
    </div>
  </template>
  
  <script>
  import ContactForm from '~/components/ContactForm.vue';
  
  export default {
    components: {
      ContactForm,
    },
  };
  </script>
  