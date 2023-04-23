<script setup>
import progressLine from "./components/progress.vue";
</script>

<template>
  <v-app>
    <!-- main -->
    <v-main style="background-color: #000825">
      <h1 class="text-white text-6xl font-bold text-center">Orders</h1>
      <p class="text-white text-center mt-10">
        this page show you the count of succes and the count of fail.
      </p>
      <v-container class="d-flex justify-center align-center text-h5">
        <!-- template of progress -->
        <progressLine />
        <!--  -->
      </v-container>
    </v-main>
  </v-app>
</template>
