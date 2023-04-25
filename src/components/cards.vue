<template>
  <div class="card" :class="{ bgSelect: bgCheck }">
    <input type="checkbox" v-model="bgCheck" />
    <h1>ID: {{ data.id }}</h1>
    <h1>Name: {{ data.name }}</h1>
    <h3>Api Key: {{ data.key }}</h3>
    <h3>Api Type: {{ data.type }}</h3>
    <h3>Account Type: {{ data.typeAcc }}</h3>
    <input type="button" value="Delete" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      bgCheck: false,
    };
  },
  props: {
    data: Object,
  },
};
</script>

<style scoped>
.card {
  transition: all 0.2s;
  display: flex !important;
  flex-direction: column;
  align-items: flex-start;
  background-color: transparent;
  border-radius: 1rem;
  box-shadow: 0 25px 50px -12px rgb(0 0 0 / 0.25);
}
.card h1 {
  font-style: normal;
  font-weight: 900;
  font-size: 29px;
  line-height: 35px;
}
.card h3 {
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 19px;
  color: #f0f0f0;
}
h3:first-of-type {
  margin-top: 2rem;
}
.card input {
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 19px;
  color: #f0f0f0;
  width: 76px;
  height: 28px;
  border-radius: 18px;
  background: #ff005c;
  align-self: flex-end;
}
.bgSelect {
  transition: all 0.2s;
  background-color: #253363 !important;
}
</style>
