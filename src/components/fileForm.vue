<script>
import theCards from "./cards.vue";

export default {
  name: "app",
  components: {
    theCards,
  },
  data() {
    return {
      arrayList: [],
      jsonData: [
        { id: 32, name: "test", api: "325543435334abfdgg" },

        { id: 32, name: "test", api: "325543435334abfdgg" },

        { id: 32, name: "test", api: "325543435334abfdgg" },
        { id: 32, name: "test", api: "325543435334abfdgg" },
      ],
    };
  },
  methods: {
    deletAll(event) {
      this.arrayList = [];
      const items = document.querySelectorAll(".bgSelect");
      for (const child of items) {
        this.arrayList.push(child.id);
      }
    },
  },
};
</script>
<template>
  <h1 class="text-white text-6xl font-bold text-center">Manage Accounts</h1>
  <p class="p-style">
    To access premium features and personalize your experience, you can
    <br />
    easily manage your account settings on our site.
  </p>
  <div class="flex-col d-flex justify-center align-center">
    <form class="form">
      <label class="custom mt-4">
        <v-file-input
          class="w-full"
          label="No file chosen"
          bg-color="#101C46"
          color="#f7f7f7f7"
          density="compact"
        ></v-file-input>
      </label>
      <input class="bg-green" type="button" value="Submit" />
      <label>Export Acount:</label>
      <input class="bg-purple" type="button" value="Export" />
      <label>Manual Import:</label>
      <input class="bg-blue" type="button" value="Import" />
      <label>Delete Selected Items:</label>
      <input class="bg-pink" type="button" value="Delete" />
    </form>
    <div class="container__cards">
      <header>
        <h1>Total Count: {{ jsonData.length }}</h1>
        <input type="button" value="Delete All" @click="deletAll" />
      </header>
      <div>
        <!-- component of cards -->
        <!-- <cards /> -->
        <theCards
          v-for="(item, index) in jsonData"
          :key="index"
          :id="index"
          :data="item"
        />
      </div>
    </div>
  </div>
</template>
<style scoped>
.mt-4 {
  margin-top: 2rem;
}
.p-style {
  margin-top: 8px;
  align-items: center;
  text-align: center;
  color: white;
}
.flex-col {
  flex-direction: column;
}

.text-6xl {
  font-size: 64px;
}

.form {
  display: grid;
  grid-template-rows: repeat(4, 1fr);
  grid-template-columns: repeat(2, 1fr);
  align-items: center;
  margin-top: 2.5rem;
  row-gap: 1rem;
  -moz-column-gap: 4rem;
  column-gap: 4rem;
}
.form input {
  width: 120px;
  font-size: 20px;
  padding: 0.5rem 0;
  border-radius: 2rem;
  color: white;
  text-align: center;
  grid-column: 2/3;
}

.form label {
  color: white;
  font-size: 18px;
  font-weight: 700;
}
.bg-green {
  background-color: #35b458d9;
}
.bg-pink {
  background-color: #ab256d;
}
.bg-blue {
  background-color: #2552ab;
}
.bg-purple {
  background-color: #6825ab;
}
.container__cards {
  margin-top: 2rem;
  display: flex;
  align-self: stretch;
  flex-direction: column;
}
.container__cards header {
  display: flex;
  padding: 1rem 2rem;
}
.container__cards header h1 {
  font-size: 30px;
}
.container__cards header input {
  margin-left: auto;
  font-weight: 700;
  background-color: #9a0a0a;
  border-radius: 1rem;
  padding: 1rem 5rem;
}
.container__cards div {
  align-self: stretch;
  background-color: #101c46;
  border-radius: 2rem;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 1rem;
  padding: 1rem;
}
</style>
