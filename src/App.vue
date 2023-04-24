<script setup>
import history from "./components/history.vue";
</script>

<!--  -->
<template>
  <div>
    <v-app>
      <v-main class="custom">
        <v-container style="align-content: space-evenly">
          <!-- template of history -->
          <history />
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
