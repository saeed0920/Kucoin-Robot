<script>
import theList from "./theList.vue";

export default {
  name: "app",
  components: {
    theList,
  },
  data() {
    return {
      jsonData: [
        {
          id: 32,
          orderId: "325543435334abfdgg",
          symbol: "BNBUSDTM",
          side: "buy",
          price: 100,
        },
        {
          id: 32,
          orderId: "325543435334abfdgg",
          symbol: "BNBUSDTM",
          side: "buy",
          price: 100,
        },
        {
          id: 32,
          orderId: "325543435334abfdgg",
          symbol: "643eafdfaa2a720001e6d444",
          side: "buy",
          price: 100,
        },
        {
          id: 32,
          orderId: "325543435334abfdgg",
          symbol: "BNBUSDTM",
          side: "buy",
          price: 100,
        },
        {
          id: 32,
          orderId: "325543435334abfdgg",
          symbol: "BNBUSDTM",
          side: "buy",
          price: 100,
        },
      ],
    };
  },
};
</script>
<template>
  <h1 class="text-white text-6xl font-bold text-center">Order History</h1>
  <p class="text-white text-center mt-10">
    Your order history is a testament to the seamless organization and <br />
    efficiency of our site, ensuring that every purchase is recorded and easily
    <br />
    accessible for your convenience.
  </p>
  <div class="item-list">
    <span></span>
    <input type="button" value="Cancel All" />
    <div class="header">
      <h1>ID</h1>
      <h1>Order_ID</h1>
      <h1>Symbol</h1>
      <h1>Side</h1>
      <h1>Size</h1>
      <h1>Price</h1>
      <h1>ReduceOnly</h1>
      <h1>Leverage</h1>
      <h1>Status</h1>
      <h1>Massage</h1>
      <h1>Created_at</h1>
      <h1>Account_name</h1>
      <h1>Cancel</h1>
    </div>

    <theList v-for="(item, index) in jsonData" :key="index" :data="item" />
  </div>
</template>

<style scoped>
.item-list {
  display: grid;
  grid-template-columns: repeat(13, 1fr);
  margin-top: 2rem;
  row-gap: 2rem;
  padding: 2rem;
  position: relative;
}
.item-list span {
  position: absolute;
  left: calc(0 + (100% / 13));
  top: 0;
  width: calc((100% / 13) * 12);
  height: 100%;
  z-index: 1;
  background: #101c46;
  border-radius: 18px;
}
.item-list:has(.list-container) span {
  grid-row-start: 3;
}
.item-list input {
  width: 257px;
  height: 50px;
  grid-row: 1 / 2;
  grid-column: 1 / -1;
  justify-self: flex-end;
  font-family: "Lato";
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  background: #9a0a0a;
  border-radius: 10px;
}
.header {
  display: grid;
  grid-template-columns: repeat(13, 1fr);
  padding: 0 0.5rem;
  gap: 1rem;
  grid-row: 2 / 3;
  grid-column: 1 / -1;
  justify-items: center;
  align-items: flex-start;
  margin: 1rem 0;
  margin-bottom: 0.5rem;
}

.header h1 {
  line-break: normal;
  font-family: "Lato";
  font-style: normal;
  font-weight: 800;
  font-size: 18px;
  line-height: 22px;
}
@media only screen and (max-width: 1300px) {
  .header h1 {
    font-size: 12px;
  }
}
</style>
