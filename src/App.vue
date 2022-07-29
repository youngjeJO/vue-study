<template>
  <ul>
    <li v-for="item in products" :key="item">
      <!-- '(item,index) in products'로 index를 추출 할 수 있음 index를 key에도 활용 가능 -->
      {{ item }}
    </li>
  </ul>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      products: ["역삼동원룸", "천호동원룸", "마포구원룸"],
    };
  },
  components: {},
};
</script>

<style></style>
