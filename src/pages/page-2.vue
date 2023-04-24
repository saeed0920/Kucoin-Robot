<script setup>
import fileForm from "./components/fileForm.vue";
</script>

<!--  -->
<template>
  <div>
    <v-app>
      <v-main class="custom">
        <v-container style="align-content: space-evenly">
          <!-- template of fileform -->
          <fileForm />
        </v-container>
      </v-main>
    </v-app>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.custom {
  background-color: #000825 !important;
  color: white;
}
</style>
