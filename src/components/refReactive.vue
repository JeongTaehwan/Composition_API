<template>
  <div>
    <div>
      <h3>{{ myInfo.name }}</h3>
      <p>{{ myInfo.age }}세</p>
    </div>
    <div>
      <h3>{{ yourInfo.name }}</h3>
      <p>{{ yourInfo.age }}세</p>
    </div>
    <button @click="CountInfoAge()">나이 증가시키기</button>
  </div>
</template>

<script>
import { ref, reactive } from "vue";

export default {
  name: "refReactive",
  setup() {
    let myInfo = ref({ name: "JeongTaehwan", age: 19 });
    let yourInfo = reactive({ name: "홍길동", age: 630 });

    const CountInfoAge = () => {
      myInfo.value.age += 1;
      yourInfo.age += 1;
    };

    return { myInfo, yourInfo, CountInfoAge };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
