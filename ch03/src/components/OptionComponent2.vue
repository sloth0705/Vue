<script>
export default {
  name: "OptionComponent2",
  // 이벤트 또는 로직 처리를 위한 함수 선언 옵션
  methods: {
    btn1Click() {
      alert("btn1 click");
    },
    btn2Click: function () {
      alert("btn2 click");
    },
    btn3Click: () => {
      alert("btn3 click");
    },
  },
};
</script>
<template>
  <h4>method option</h4>
  <button v-on:click="btn1Click">button1</button>
  <button @click="btn2Click">button2</button>
  <button @click="btn3Click">button3</button>
</template>
<style scoped></style>
