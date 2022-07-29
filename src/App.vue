<template>
  <ul>
    <li v-for="(item, index) in products" :key="index">
      <!-- '(item,index) in products'로 index를 추출 할 수 있음 index를 key에도 활용 가능 -->
      {{ item }}
      <button @click="increase(index)">신고하기</button>
      <span>신고수 : {{ 신고[index] }}</span>
    </li>
  </ul>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      products: ["역삼동원룸", "천호동원룸", "마포구원룸", "동작구원룸"],
      신고: new Array(this.products),
    };
  },
  methods: {
    increase(index) {
      if (!this.신고[index]) {
        this.신고[index] = 1;
      } else {
        this.신고[index] += 1;
      }
    },
  },
  components: {},
};
</script>

<style></style>
