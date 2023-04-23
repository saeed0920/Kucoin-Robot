<template>
  <div>
    <v-progress-linear
      style="background-color: #59607b"
      v-model="percent"
      height="25"
      color="deep-orange"
      rounded
    >
      <strong class="text-white"> {{ percent }}%</strong>
    </v-progress-linear>

    <div
      class="grid grid-rows-[minmax(max-content,_1fr)] grid-cols-2 mt-12 gap-10"
    >
      <p
        class="text-white leading-5 text-base font-medium p-8 bg-[#17203D] rounded-lg"
      >
        Succes Count: {{ succes }}
      </p>
      <p
        class="text-white leading-5 text-base font-medium p-8 bg-[#17203D] rounded-lg"
      >
        Fail Count: {{ fail }}
      </p>
      <p
        class="text-white leading-5 text-base font-medium p-8 bg-[#17203D] rounded-lg"
      >
        Total Count: 130 {{ total }}
      </p>
      <p
        class="text-white leading-5 text-base font-medium p-8 bg-[#17203D] rounded-lg"
      >
        Message: Your Massage {{ message }}
      </p>
      <p
        class="text-white leading-5 text-base font-medium p-8 bg-[#17203D] rounded-lg col-span-full"
      >
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
  methods: {},
};
</script>
