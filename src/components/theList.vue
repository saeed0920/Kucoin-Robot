<script>
export default {
  props: {
    data: Object,
  },
};
</script>
<template>
  <div class="list-container">
    <span></span>
    <h3>{{ data.id }}</h3>
    <h3>{{ data.symbol }}</h3>
    <h3>{{ data.side }}</h3>
    <h3>{{ data.price }}</h3>
    <h3>{{ data.price }}</h3>
    <h3>{{ data.price }}</h3>
    <h3>{{ data.price }}</h3>
    <h3>{{ data.price }}</h3>
    <h3>{{ data.price }}</h3>
    <h3>{{ data.price }}</h3>
    <h3>{{ data.price }}</h3>
    <h3>{{ data.price }}</h3>

    <input type="button" value="Cancel" />
  </div>
</template>

<style scoped>
.list-container {
  z-index: 2;
  max-width: 100%;
  padding: 1rem 0;
  display: grid;
  grid-template-columns: repeat(13, 1fr);
  gap: 1rem;
  grid-column: 1 / -1;
  padding: 1rem 0.5rem;
  justify-items: center;
  align-items: center;
  position: relative;
}
.list-container span {
  position: absolute;
  bottom: -100%;
  left: 0;
  height: 1px;
  background-color: rgba(90, 163, 255, 0.4);
  width: calc((100% / 13) * 12);
}
.list-container > * {
  grid-row: 1 / 2;
}
.list-container:hover {
  background: #253363;
}
.list-container h3 {
  line-break: anywhere;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 17px;
  color: #ffffff;
}
.list-container input {
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 19px;
  background: #ff005c;
  border-radius: 18px;
  width: 76px;
  height: 28px;
}
@media only screen and (max-width: 1300px) {
  .list-container h3 {
    font-size: 12px;
  }
}
</style>
