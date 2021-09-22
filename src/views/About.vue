<template>
  <div class="about">
    <div
      :style="{ backgroundImage: `url(${$store.state.Portfolio[0].mainImg})` }"
    ></div>
    <h1>{{ $store.state.Portfolio[0].mainTitle }}</h1>
    <h6>{{ $store.state.Portfolio[0].mainText }}</h6>
    <img :src="`${$store.state.Portfolio[0].img1}`" alt="" />
  </div>
</template>
<script>
export default {};
</script>
<style>
body,
html {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
}
.about {
  width: 100%;
}
.about div {
  width: 300px;
  height: 300px;
}
h1 {
  font-size: 14px;
}
img {
  width: 500px;
  height: 500px;
}
</style>
