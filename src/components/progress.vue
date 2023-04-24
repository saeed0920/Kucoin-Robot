<template>
  <h1 class="text-white text-6xl font-bold text-center">Orders</h1>
  <p class="text-white text-center mt-10">
    this page show you the count of succes and the count of fail.
  </p>

  <div class="d-flex justify-center align-center text-h5">
    <v-progress-linear
      style="background-color: #59607b"
      v-model="percent"
      height="25"
      color="#2E008F"
      rounded
    >
      <strong class="text-white"> {{ percent }}%</strong>
    </v-progress-linear>

    <div class="custom-display">
      <p class="text-white p-styles">Succes Count: {{ succes }}</p>
      <p class="text-white p-styles">Fail Count: {{ fail }}</p>
      <p class="text-white p-styles">Total Count: 130 {{ total }}</p>
      <p class="text-white p-styles">Message: Your Massage {{ message }}</p>
      <p class="text-white col-span-full p-styles">
        Erros: <br />
        {{ errors }}
      </p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      percent: 33,
      succes: 100,
      fail: 30,
      total: this.succes + this.fail,
      message: "You message",
      errors:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis enim lobortis scelerisque fermentum dui faucibus in ornare quam. Vitae sapien pellentesque habitant morbi tristique senectus et netus et. Sit amet consectetur adipiscing elit pellentesque habitant morbi. In egestas erat imperdiet sed euismod nisi porta lorem mollis. Enim neque volutpat ac tincidunt vitae semper quis lectus. Ipsum consequat nisl vel pretium lectus quam. Varius duis at consectetur lorem donec massa sapien faucibus. Amet cursus sit amet dictum sit amet justo. Pulvinar sapien et ligula ullamcorper malesuada. Aliquam id diam maecenas ultricies mi. Amet massa vitae tortor condimentum lacinia quis. Tellus rutrum tellus pellentesque eu tincidunt tortor. Blandit turpis cursus in hac habitasse. Diam donec adipiscing tristique risus. Tincidunt ornare massa eget egestas purus. Vestibulum sed arcu non odio euismod lacinia at. Leo vel orci porta non pulvinar neque laoreet. Enim nunc faucibus a pellentesque sit amet. Dui nunc mattis enim ut tellus elementum sagittis. ",
    };
  },
};
</script>

<style scoped>
.custom-display {
  display: grid;
  grid-template-rows: minmax(max-content, 1fr);
  grid-template-columns: repeat(2, 1fr);
  margin-top: 3rem;
  gap: 1.5rem;
}

.p-styles {
  line-height: 1.25rem;
  font-size: 1rem;
  font-weight: 500;
  padding: 2rem;
  background-color: #17203d;
  border-radius: 0.5rem;
}
.col-span-full {
  grid-column: 1 / -1;
}

.text-white {
  color: white;
}
</style>
