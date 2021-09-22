<template>
  <div class="about">
    <div
      :style="{ backgroundImage: `url(${$store.state.Portfolio[0].mainImg})` }"
    ></div>
    <h1>{{ $store.state.Portfolio[0].mainTitle }}</h1>
    <h6>{{ $store.state.Portfolio[0].mainText }}</h6>
    <img :src="`${$store.state.Portfolio[0].img1}`" alt="" />
    <p>
      {{ $store.state.Portfolio[0].type }}
    </p>
    <p>
      {{ $store.state.Portfolio[0].concept }}
    </p>
    <p class="event" v-if="fade === 1">
      {{ $store.state.Portfolio[0].subText }}
    </p>
    <button @click="event()">좌표확인</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      fade: 0,
    };
  },
  methods: {
    event() {
      const div = document.querySelector(".event");
      const divRect = div.getBoundingClientRect().y;
      if (divRect < 1050) {
        this.fade = 1;
      }
    },
  },
};
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
button {
  width: 200px;
  height: 50px;
}
</style>
