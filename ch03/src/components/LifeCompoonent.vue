<script>
export default {
  name: "LifeComponent",
  methods: {
    btnAdd: function () {
      this.count++;
    },
  },
  data() {
    return {
      count: 0,
    };
  },
  // 컴포넌트 라이프 사이클 함수(Hook)
  beforeCreate: function () {},
  created: function () {},
  beforeMount: function () {},
  mounted: function () {},
  beforeUpdate: function () {},
  updated: function () {},
  beforeUnmount: function () {},
  unmounted: function () {},
};
</script>
<template>
  <h4>LifeComponent</h4>
  <p>카운터: {{ count }}</p>
  <button @click="btnAdd">증가</button>
</template>
<style scoped></style>
