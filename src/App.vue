<script setup>
import fileForm from "./components/fileForm.vue";
</script>

<template>
  <v-app>
    <!-- main -->
    <v-main style="background-color: #000825">
      <h1 class="text-white text-6xl font-bold text-center">Manage Accounts</h1>
      <p class="text-white text-center mt-10">
        To access premium features and personalize your experience, you can
        <br />
        easily manage your account settings on our site.
      </p>
      <v-container class="d-flex justify-center align-center text-h5">
        <!-- template of fileform -->
        <fileForm />
        <!--  -->
      </v-container>
    </v-main>
  </v-app>
</template>
